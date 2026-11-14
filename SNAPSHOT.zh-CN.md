# REA 源码快照

这份私有仓库是用户要求保存的 [morluto/rea](https://github.com/morluto/rea) 完整已跟踪源码快照，保留原 README、LICENSE、THIRD_PARTY_NOTICES、licenses、源码、文档、资源、测试及 Git 文件模式。

- 上游版本：6.9.0。
- 固定提交：`2343e5692595ae9c08ce7de5bb91460118e67ed2`。
- 保存日期：2026-11-14。
- 上游版权：Copyright (c) 2026 morluto；许可为 MIT。第三方材料仍适用各自许可证，参见原许可与通知文件。
- 五个上游子模块保留 `.gitmodules` 和固定 Git 提交引用；没有自动下载第三方工具。需要相关能力时按上游文档初始化对应子模块。

原上游文件没有因本次保存而修改。此仓库新增的说明只有本文件和 `UPSTREAM.json`；本地依赖、编译产物、临时浏览器资料和网页原始脚本没有加入源码仓库。

## 使用方式

REA 是提供 CLI/MCP 的本地逆向分析工具，网站与 JavaScript 静态分析不需要 Hopper、IDA 或 Ghidra，也不需要模型 API 密钥。直接使用源仓库需遵照原 README 安装依赖并编译。上游当前要求 Node.js `^22.23.4 || ^24.22.1 || >=26.12.1`。

若仅使用已发布 CLI，可在隔离目录获取官方固定版本 `rea-agents@6.9.0`，然后调用 `rea --help`。全局 MCP 注册与 `rea setup` 是另外的安装操作，本次没有运行，也没有更改用户现有全局 Node、Codex 或 MCP 配置。

## 本次在观潮看盘中的实际用途

观潮项目依据用户提供的大盘云图参考站，读取公开交付的前端资源，使用 REA 的 `analyze-javascript-application` 离线分析入口检查主渲染脚本，并结合实际页面截图改进云图。REA 分析结果属于静态代码证据，不能证明所有代码分支的运行可达性，也不能重建服务端源码。

分析记录和项目更新入口见 [aHao030/guanchao-kanpan](https://github.com/aHao030/guanchao-kanpan) 的 `docs/reverse-engineering/rea-report.md`。大盘云图原始脚本仅用于本地分析，不作为本仓库或看盘项目的再分发代码。
