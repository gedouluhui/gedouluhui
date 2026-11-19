### LuHui

两类东西，都是**离线、可复核、能自己改**的：

1. **本地优先的 Windows 桌面工具** —— 不套 Electron 壳、不接账号、不埋统计。
2. **「可执行证据」校验工具** —— 拿你真实的输入跑一遍，产出带哈希的报告和可复现的 PASS / FAIL，而不是一句「看起来没问题」。

---

#### 桌面工具

| 项目 | 一句话 | 技术 |
|---|---|---|
| [LuHui播放器](https://github.com/gedouluhui/luhui-player) | mpv 当内核、手绘 Fluent 外壳的本地视频播放器；硬解 / HDR / 真实帧缩略图 | Python · PyQt5 · mpv |
| [LuHui音乐播放器](https://github.com/gedouluhui/luhui-music-player) | WinUI 3 外壳 + 本地音频服务 + WASAPI 独占 / 逐位直通 | C# · WinUI 3 · Python |
| [番茄闹钟](https://github.com/gedouluhui/fanqie-alarm) | 整个应用就是一个 HTML 的番茄钟；零依赖、零网络请求 | HTML · C# · WebView2 |
| [pc-phone-proxy](https://github.com/gedouluhui/pc-phone-proxy) | 电脑 + 安卓双端自动选线，自建节点池、敏感域直连 | Python · Java · sing-box / Xray |

#### 可执行证据

| 方向 | 项目 |
|---|---|
| 训练与推理 | [resumetrace](https://github.com/gedouluhui/resumetrace)（跨真实进程退出的断点恢复）· [stepcontract](https://github.com/gedouluhui/stepcontract)（训练步契约）· [mergeproof](https://github.com/gedouluhui/mergeproof)（LoRA 合并核验）· [weight-witness](https://github.com/gedouluhui/weight-witness)（safetensors 分片归属）· [attnwitness](https://github.com/gedouluhui/attnwitness)（注意力掩码见证）· [roundoff-lab](https://github.com/gedouluhui/roundoff-lab)（量化误差诊断）· [stride-lens](https://github.com/gedouluhui/stride-lens)（张量布局与别名） |
| 数据与检索 | [vector-result-audit](https://github.com/gedouluhui/vector-result-audit)（并列感知的召回与过滤泄漏）· [maskledger](https://github.com/gedouluhui/maskledger)（COCO 分割转换损失）· [installscope](https://github.com/gedouluhui/installscope)（wheel 安装目标冲突） |
| 文本与接口 | [chat-input-contract](https://github.com/gedouluhui/chat-input-contract)（分词与模板漂移）· [schema-boundary](https://github.com/gedouluhui/schema-boundary)（JSON Schema 语义兼容反例）· [stream-contract](https://github.com/gedouluhui/stream-contract)（SSE / 流式客户端边界）· [bitequiv](https://github.com/gedouluhui/bitequiv)（定宽整数改写等价性） |
| 文档与数据 | [plotproof](https://github.com/gedouluhui/plotproof)（Matplotlib 导出 PDF 的文字证据）· [frameledger](https://github.com/gedouluhui/frameledger)（抽帧时间戳契约）· [planbench-sqlite](https://github.com/gedouluhui/planbench-sqlite)（同一快照上比 SQL 与索引） |

**共同点**：只读本机文件或只处理本机数据；该离线的一律离线，需要联网的把开关和流量路径写清楚；每个仓库都带自己的构建步骤和验收脚本 —— 信 README 之前先跑一遍。

中文为主，代码与报告尽量双语。欢迎提 issue 拍砖，也欢迎直接拿去做你自己的项目的「证据层」。

---

*Local-first Windows tools and offline "executable evidence" checkers. No Electron shells, no accounts, no telemetry. Each repository ships its build steps and its verification suite — read and run them before trusting the README.*
