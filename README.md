# Sub-Agent Manager Skill for OpenClaw

[中文版](#中文介绍) | [English Version](#english-description)

---

<a name="english-description"></a>
## English Description

A "Supervisor Mode" skill designed for OpenClaw that optimizes task execution and user experience.

### Core Features
- **🚀 Instant Response**: As a supervisor, the agent immediately acknowledges receipt and shares the execution plan, eliminating user wait time.
- **Parallel Task Delegation**: Supports decomposing complex tasks and distributing them to multiple sub-agents for concurrent execution.
- **🤖 Automatic Progress Reports**: Built-in monitoring logic that automatically updates the user on task status every 3-5 minutes for long-running jobs.
- **🎯 Management Focus**: Adheres to the philosophy that "managers don't do the grunt work," focusing instead on scheduling, monitoring, and result synthesis.
- **⚡ Speed + Depth Architecture**: Optimized for a hybrid setup where a **Flash model** acts as the high-speed supervisor while **Thinking models** serve as specialized sub-agents for complex execution.

### Installation & Usage
Copy this folder into your OpenClaw skills directory.

### Workflow
1. **Receive Task**: Supervisor receives instructions and formulates a plan.
2. **Spawn Sub-agents**: Launches sub-agents via `sessions_spawn` for specific tasks.
3. **Instant Feedback**: Notifies the user of the dispatch and provides session IDs.
4. **Progress Monitoring**: For long tasks, sets up periodic checks via Cron.
5. **Result Synthesis**: Synthesizes and reports the final outcome in a standardized format.

---

<a name="中文介绍"></a>
## 中文介绍

这是一个为 OpenClaw 设计的“主管模式” (Supervisor Mode) 技能，旨在优化任务执行效率与用户交互体验。

### 核心特性
- **🚀 秒回响应**：作为主管，Agent 会立即确认收到任务并告知计划，绝不让用户处于等待状态。
- **并行任务分配**：支持将复杂任务拆解并分发给多个子进程 (Sub-agents) 并行执行，极大提升效率。
- **🤖 自动进度汇报**：内置定时检查机制，对于耗时任务会自动定期向用户汇报当前进度，让过程透明化。
- **🎯 专注管理**：遵循“管理者不亲自干活”的哲学，专注于任务调度、监控和结果汇总。
- **⚡ 速度与深度架构**：建议使用 **Flash 模型**（如 Gemini 3 Flash）作为高速主管负责即时回复与协调，并指派 **深度思考模型**（如 Claude 3.5 Sonnet, DeepSeek R1）作为子进程负责复杂任务的执行。

### 安装与使用
将此文件夹放入你的 OpenClaw 技能目录中即可激活。

### 工作流
1. **接收任务**：主管接收用户指令并制定执行计划。
2. **派发子进程**：通过 `sessions_spawn` 启动子进程执行具体工作。
3. **即时反馈**：立即告知用户子进程已派出及相关 ID。
4. **进度监控**：对于长耗时任务，自动建立 Cron 任务进行进度巡检。
5. **结果汇总**：子进程完成后，主管提取结果并以标准格式向用户汇报。

---
Driven by the OpenClaw Community.
