# iPTV 公开源 · 影视仓订阅

把 [anlianchui/iptv2](https://github.com/anlianchui/iptv2)（iPTV v4.46.0）仓库里的公开直连源，
优化成可直接粘贴到**影视仓 / TVBox** 的直播接口。

## 在线链接

| 文件 | 用途 |
| --- | --- |
| `https://cdn.jsdelivr.net/gh/anlianchui/IPTVnew@main/tvbox.json` | **推荐**。影视仓 / TVBox 配置地址 |
| `https://cdn.jsdelivr.net/gh/anlianchui/IPTVnew@main/tvbox-https.json` | **播放失败先试这个**。纯 HTTPS，63 频道，每个都能播 |
| `https://cdn.jsdelivr.net/gh/anlianchui/IPTVnew@main/tvbox-full.json` | 完整版，额外含大陆不可达的频道（海外用） |
| `https://cdn.jsdelivr.net/gh/anlianchui/IPTVnew@main/tvbox-cctv-ipv6.json` | CCTV-1~17 完整版，需 IPv6 网络 |
| `https://cdn.jsdelivr.net/gh/anlianchui/IPTVnew@main/live.m3u` | 标准 M3U，带台标，适合 TiviMate / APTV / Kodi |
| `https://cdn.jsdelivr.net/gh/anlianchui/IPTVnew@main/live.txt` | 纯文本「频道名,地址」，兼容性最好 |

影视仓入口：**设置 → 直播 → 添加直播源**（或首页顶部切到直播）。

**播放黑屏先看这里**：Android 默认禁止明文流量，带 `http://` 线路的频道会直接黑屏。
优先用 `tvbox-https.json`（纯 HTTPS，63 个频道全部可播）；
`tvbox.json` 里同一频道已把 HTTPS 线路排到首位，但仍有 20 个频道只有明文线路。
老版本不认 JSON 就用 `live.txt`。

托管仓库：<https://github.com/anlianchui/IPTVnew>

## 关于 CCTV

**iPTV 仓库的静态列表里一条央视都没有**，这不是被删了，而是设计如此：

- 央视被放在「央视频直播」抓取模块里（63 个公开频道 + 10 个会员频道）
- 该模块需要**部署服务端动态取票**，拿不到固定直连地址，所以不会写进仓库的 `IPTV.m3u`

因此本列表的「央视频」分组是从 [iptv-org/iptv](https://github.com/iptv-org/iptv) 的公开条目补齐的，
共 16 个频道：`CCTV-1 / 2 / 3 / 4中文国际 / 7 / 8 / 9 / 10 / 11 / 12 / 13 / 14 / 15 / 16 / 17 / 8K`。

**缺 CCTV-5（体育）、CCTV-5+、CCTV-6（电影）**：IPv4 公开转发站基本没有这三个，
可用的都是 IPv6 地址，已单独放在 `tvbox-cctv-ipv6.json`（需要播放设备所在网络支持 IPv6）。

## 本次优化做了什么

| 优化项 | 说明 |
| --- | --- |
| 存活探测 | 逐条取流验证，剔除确认失效的源（如 UFC 24/7 返回 `Invalid sessionId`） |
| HTTPS 升级 | `http://` 能升 https 的就升。Android 9+ 默认禁明文流量，不升影视仓会黑屏 |
| 剔除 RTMP | 影视仓播放器不支持 RTMP，直接删 |
| 补全台标 | 用仓库自带 `logo-pack/index.json` 补 `tvg-logo`；过滤掉其中 45 条「来源说明文字」而非图片地址的脏数据 |
| 清洗注释 | 去掉 `# === BEGIN/END ===`、`# 实验台备注` 等注释块与空行 |
| 格式规范 | 统一 `#EXTINF` 属性顺序，去掉空的 `tvg-logo=""` |
| 编码统一 | UTF-8 无 BOM + LF 换行 |
| 分组重排 | 按影视仓使用习惯排序，央视频置顶 |

当前推荐版：**13 个分组 / 81 个频道**（完整版 89，CCTV IPv6 版 18）。

## 文件说明

| 文件 | 说明 |
| --- | --- |
| `tvbox.json` | 推荐版，只含探测确认可用的源 |
| `tvbox-full.json` | 完整版，额外含 14 条沙箱网络不可达的源 |
| `tvbox-cctv-ipv6.json` | CCTV 完整版（IPv6 直连，未验证） |
| `live.m3u` / `live-full.m3u` | M3U 格式 |
| `live.txt` / `live-full.txt` | TXT 格式 |
| `live-ext.m3u` | 第三方转发站源，项目方明确不维护 |
| `probe-report.md` | 探测明细报告 |
| `build.py` | 生成脚本 |

## 重新生成

```bash
python3 build.py                   # 从 GitHub 拉最新源 + 实时探测
python3 build.py --no-probe        # 跳过实时探测，用上次缓存（快）
python3 build.py --epg <地址>      # 指定 EPG 节目单，写进 m3u 的 x-tvg-url
```

EPG 默认不写：公开 EPG 源地域差异大，实测大陆出口下 `epg.112114.eu.org`、
`epg.aptvapp.com` 均不可达，挂一个取不到的 EPG 会明显拖慢起播。
需要节目单时自己挑一个能通的再传 `--epg`。

## 注意

- 探测只代表「这一刻能取到流」，直播源随时可能失效。
- 探测出口是**大陆网络**：Bloomberg、DW、第三方转发站在大陆不可达，
  已归入「网络不可达」并只放进完整版；海外网络请用 `tvbox-full.json`。
- 保留的少数 `http://` 明文源（台湾几条 IP 直连）无法升级，
  影视仓需自行允许明文流量。
- 本项目仅做公开地址的整理与格式转换，不托管任何节目内容。
  请在你拥有合法授权的范围内使用。
