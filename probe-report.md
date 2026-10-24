# 探测与优化报告

生成时间：2026-10-24 17:20:02 CST
探测范围：133 条源（精选 30 + 海外 42 + 第三方 61）

| 结果 | 数量 | 处理方式 |
| --- | --- | --- |
| 确认可用 | 83 | 进入推荐版 |
| 网络不可达 | 48 | 只进完整版，多为出口地域限制 |
| 确认失效 | 2 | 剔除 |
| RTMP 不支持 | 2 | 剔除 |

HTTPS 升级 2 条，补全台标 42 条。

## 数据来源

- GitHub https://raw.githubusercontent.com/anlianchui/iptv2/main/IPTV.m3u
- GitHub https://raw.githubusercontent.com/anlianchui/iptv2/main/IPTV-overseas.m3u
- CCTV 补充源 · GitHub https://cdn.jsdelivr.net/gh/iptv-org/iptv@master/streams/cn.m3u
- CCTV 完整版(IPv6) · GitHub https://cdn.jsdelivr.net/gh/fanmingming/live@main/tv/m3u/ipv6.m3u

## 推荐版分组统计

| 分组 | 频道数 |
| --- | --- |
| 央视频 | 18 |
| 卫视 | 2 |
| 体育 | 17 |
| 国际 | 8 |
| 文旅 | 10 |
| 娱乐时尚 | 12 |
| 香港 | 1 |
| 台湾 | 5 |
| 江苏 | 6 |
| 福建 | 1 |
| 青海 | 1 |
| 宠物 | 1 |
| 韩国 | 1 |
| **合计** | **83** |

## 网络不可达（仅收录进完整版）

| 分组 | 频道 | 地址 | 探测结果 |
| --- | --- | --- | --- |
| 文旅 | Terra Mater WILD | `https://amg01775-amg01775c1-amgplt0343.playout.now3.amagi.tv` | 无响应（超时 / 不可达 / DNS 失败） |
| 国际 | Bloomberg TV Asia | `https://www.bloomberg.com/media-manifest/streams/asia.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 国际 | Bloomberg TV Europe | `https://www.bloomberg.com/media-manifest/streams/eu.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 国际 | Bloomberg TV US | `https://www.bloomberg.com/media-manifest/streams/us.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 国际 | DW English | `https://dwamdstream102.akamaized.net/hls/live/2015525/dwstre` | 无响应（超时 / 不可达 / DNS 失败） |
| 央视频 | CCTV-1 | `http://69.30.245.50/live/cctv1.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 央视频 | CCTV-1 | `http://198.204.240.250:82/live/cctv1.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 央视频 | CCTV-4K | `http://198.204.240.250:82/live/cctv4k.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 央视频 | CCTV-5+ | `https://myip.pdtvhd.com/Sports/streams/CCTV5pul.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 央视频 | CCTV-6 | `http://69.30.245.50/live/cctv6.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 央视频 | CCTV-6 | `http://198.204.240.250:82/live/cctv6.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 央视频 | CCTV-6 | `https://live.eac-news.com/CCTV/streams/cctv6.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 央视频 | CCTV-8K | `http://198.204.240.250:82/live/cctv8k.m3u8` | 无响应（超时 / 不可达 / DNS 失败） |
| 央视频 | CCTV-13 | `http://go.bkpcp.top/mg/cctv13` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | TVB新闻 | `https://cdn6.cc.cd/163189/wxxw` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | 明珠台 | `https://cdn.qd.je/163189/mzt` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | TVB娱乐新闻台 | `https://cdn6.cc.cd/163189/ylxw` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | TVB1 | `https://cdn6.cc.cd/163189/tvb1` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | TVBJ1 | `https://cdn6.cc.cd/163189/j1` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | 无线新闻台 | `https://cdn6.cc.cd/163189/wxxwt` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | HOY TV | `https://cdn.qd.je/163189/hoy` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | HOY资讯台 | `https://cdn.qd.je/163189/hoy78` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | HOY国际财经台 | `https://cdn.qd.je/163189/hoy76` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | NOW新闻台 | `https://cdn.qd.je/163189/now` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | RTHK31 | `https://cdn.qd.je/163189/rthk31` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | RTHK32 | `https://cdn.qd.je/163189/rthk32` | 无响应（超时 / 不可达 / DNS 失败） |
| 香港 | 凤凰香港 | `https://cdn.qd.je/163189/fhhk` | 无响应（超时 / 不可达 / DNS 失败） |
| 澳门 | 澳视澳门 | `https://cdn.qd.je/163189/asam` | 无响应（超时 / 不可达 / DNS 失败） |
| 澳门 | 澳视卫星 | `https://cdn.qd.je/163189/as` | 无响应（超时 / 不可达 / DNS 失败） |
| 澳门 | 澳门体育 | `https://cdn.qd.je/163189/amty` | 无响应（超时 / 不可达 / DNS 失败） |
| 澳门 | 澳门综艺 | `https://cdn.qd.je/163189/amzy` | 无响应（超时 / 不可达 / DNS 失败） |
| 澳门 | 澳门莲花 | `https://cdn.qd.je/163189/amlh` | 无响应（超时 / 不可达 / DNS 失败） |
| 新加坡 | CH5 | `https://cdn.qd.je/163189/ch5` | 无响应（超时 / 不可达 / DNS 失败） |
| 新加坡 | CH8 | `https://cdn.qd.je/163189/ch8` | 无响应（超时 / 不可达 / DNS 失败） |
| 新加坡 | CHU | `https://cdn.qd.je/163189/chu` | 无响应（超时 / 不可达 / DNS 失败） |
| 马来西亚 | Astro AOD | `https://cdn.qd.je/163189/aod` | 无响应（超时 / 不可达 / DNS 失败） |
| 马来西亚 | Astro欢喜台 | `https://cdn.qd.je/163189/hxt` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | TVB星河 | `https://cdn6.cc.cd/163189/tvbxh` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | TVB亚洲武侠 | `https://cdn6.cc.cd/163189/yzwx` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | 重温经典 | `https://cdn.qd.je/163189/cwjd` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | 龙华电影 | `https://cdn.qd.je/163189/lhdy` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | 龙华经典 | `https://cdn.qd.je/163189/lhjd` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | 龙华偶像 | `https://cdn.qd.je/163189/lhox` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | 龙华日韩 | `https://cdn.qd.je/163189/lhrh` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | 龙华戏剧 | `https://cdn.qd.je/163189/lhxj` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | 龙华洋片 | `https://cdn.qd.je/163189/lhyp` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | 龙华卡通 | `https://cdn.qd.je/163189/lhkt` | 无响应（超时 / 不可达 / DNS 失败） |
| 影视 | 天映频道 | `https://cdn.qd.je/163189/typd` | 无响应（超时 / 不可达 / DNS 失败） |

## 确认失效（已剔除）

| 分组 | 频道 | 地址 | 原因 |
| --- | --- | --- | --- |
| 体育 | UFC 24/7 | `https://dbrb49pjoymg4.cloudfront.net/manifest/3fec3e5cac39a5` | 返回非直播内容：{"message":"Invalid sessionId [1 |
| 国际 | TRT World | `https://tv-trtworld.medya.trt.com.tr/master.m3u8` | 返回非直播内容：Mk05-'n!QzatS;$Y?<҂Bj\|^CY\|r!3a |

## 说明

- 探测只判断「现在这一刻能否取到清单/分片」，不代表长期稳定，平台随时会换地址。
- 探测出口是**大陆网络**：Bloomberg、DW、第三方转发站等在大陆不可达，会被归入「网络不可达」。如果你在海外，改用 `tvbox-full.json` / `live-full.*`。
- `http://` 源已尽量升级为 `https://`（Android 9+ 默认禁止明文流量，不升级影视仓会黑屏）；改不了的保留明文，需在影视仓设置里允许明文流量。
- 第三方源（from-the-web）项目方明确不维护、不保证可用，已单独输出为 `live-ext.m3u`，按需自行添加。
