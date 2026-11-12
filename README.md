### LuHui

独立开发 Windows 桌面工具，偏好**本地优先、零联网、能自己改**的东西。
不做 Electron 套壳，不接账号体系，不埋统计。

| 项目 | 一句话 | 技术 |
|---|---|---|
| [LuHui播放器](https://github.com/gedouluhui/luhui-player) | mpv 当内核、手绘 Fluent 外壳的本地视频播放器；真实帧缩略图、12 项画面调整 | Python / PyQt5 / mpv |
| [LuHui音乐播放器](https://github.com/gedouluhui/luhui-music-player) | WinUI 3 外壳 + 本地音频服务 + WASAPI 独占 / 逐位直通 | C# / WinUI 3 / Python |
| [番茄闹钟](https://github.com/gedouluhui/fanqie-alarm) | 整个应用就是一个 HTML 的番茄钟；零依赖、零网络请求 | HTML / C# / WebView2 |
| [pc-phone-proxy](https://github.com/gedouluhui/pc-phone-proxy) | 电脑 + 安卓双端自动选线，自建节点池、敏感域直连 | Python / Java / sing-box / Xray |

**共同点**：只读本机文件或只处理本机数据；不联网的就不联网，需要联网的把开关和流量路径写清楚。
源码全部公开，欢迎提 issue 拍砖。

---

*Local-first Windows tools. No Electron shells, no accounts, no telemetry.
Each repo ships its build steps and its verification suite — read them before trusting the README.*
