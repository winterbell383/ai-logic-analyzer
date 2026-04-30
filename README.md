# ai-logic-analyzer
结合 sigrok 与 AI Agent 的逻辑分析仪波形解析工具
# 🚀 AI Logic Analyzer (MCP-Sigrok)

> 🚧 **Work In Progress (WIP)**: 本项目目前处于早期构思与开发阶段。

本项目旨在通过 Anthropic 的 **MCP (Model Context Protocol)**，将传统的开源逻辑分析仪工具（基于 `sigrok` / `PulseView`）与 LLM AI Agent（如 Claude Code）结合起来。

让 AI 帮你“看”波形、查手册、找 Bug！

## 💡 为什么做这个项目？
在嵌入式开发中，阅读逻辑分析仪抓取的 I2C、SPI、UART 长串十六进制波形数据耗时且枯燥。
由于市面上常见的 24MHz FX2 逻辑分析仪拥有庞大的用户基础，我们希望写一个中间件，将 `sigrok-cli` 解析出的底层电平信号清洗为结构化 JSON 数据，直接喂给大模型进行自动协议诊断。

## ✨ 核心特性（规划中）
- [x] 项目初始化与构思
- [ ] 封装 `sigrok-cli`，支持读取离线 `.sr` 文件
- [ ] 基于 FastMCP 暴露本地工具接口
- [ ] 支持 I2C 协议清洗与 AI 分析（ACK/NACK 异常检测）
- [ ] 支持 UART / SPI 协议分析
- [ ] 输出高价值的结构化通信 Transaction 序列

## 🛠️ 技术栈
- **硬件**: Saleae 兼容 24MHz/8CH 逻辑分析仪 (FX2)
- **底层解析**: [sigrok-cli](https://sigrok.org/)
- **AI 协议**: [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)
- **开发语言**: Python 3.10+

## 👨‍💻 关于作者
大三学生，热爱嵌入式与 AI 技术。欢迎各路大佬提 Issue 或 PR 共同完善！
