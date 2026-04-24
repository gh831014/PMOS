# PMOS 使用手册 / PMOS User Guide

**版本 Version**: 3.34  
**系统 System**: Personal Multi-Agent Operating System  
**底层引擎 Backend**: OpenClaw / WorkCow

---

## 目录 / Table of Contents

1. [系统概述 / System Overview](#1-系统概述--system-overview)
2. [核心模块 / Core Modules](#2-核心模块--core-modules)
3. [OpenClaw vs Hermes vs PMOS 对比](#3-openclaw-vs-hermes-vs-pmos-对比)
4. [快速开始 / Quick Start](#4-快速开始--quick-start)
5. [配置管理 / Configuration](#5-配置管理--configuration)
6. [常见问题 / FAQ](#6-常见问题--faq)

---

## 1. 系统概述 / System Overview

### 什么是 PMOS？

PMOS (Personal Multi-Agent Operating System) 是一款面向未来的个人多Agent操作系统。它将多个AI Agent视为独立的"员工"，通过协同工作帮助用户完成复杂任务。

PMOS is a next-generation Personal Multi-Agent Operating System that treats multiple AI Agents as independent "employees" working together to help users accomplish complex tasks.

### 核心定位 / Core Positioning

```
┌─────────────────────────────────────────────────────────────┐
│                     PMOS 核心定位                            │
├─────────────────────────────────────────────────────────────┤
│  🎯 定位: 个人AI团队管理系统                                  │
│  👥 协作: 多Agent圆桌会议决策                                 │
│  🔒 安全: 通信白名单 + 定期校验机制                            │
│  🚀 效率: 自主可控底层 + 智能路由                               │
└─────────────────────────────────────────────────────────────┘
```

### 系统架构 / System Architecture

```
Layer 1: 前端接入层 (Frontend Layer)
├── Web App (PWA)
├── Mobile (React Native)
├── Desktop (Electron)
└── CLI

Layer 2: 服务层 (Service Layer)
├── 🖥️ NEXUS 决策系统
├── 🏰 记忆宫殿系统
├── 👤 人格塑造系统
└── 🌐 协同安全机制

Layer 3: 执行能力层 (Execution Layer)
├── 🤖 Agent 服务
├── 📋 任务调度器
└── ⚡ 协作服务

Layer 4: 规范层 (Harness Layer)
├── 📜 Agent 准则
├── 🔧 专业准则
└── ✅ 执行准则

Layer 5: 底层适配层 (Adapter Layer) ⭐
├── OpenClaw Mode (API网关)
└── WorkCow Mode (自主可控) ✨

Layer 6: 基础设施层 (Infrastructure)
└── SQLite + SQLite-Vector
```

---

## 2. 核心模块 / Core Modules

PMOS 提供九大核心模块，涵盖AI协作的完整生命周期：

PMOS provides nine core modules covering the complete lifecycle of AI collaboration:

| # | 模块 Module | 图标 Icon | 功能 Function |
|---|-------------|-----------|---------------|
| 1 | **NEXUS决策系统** | 🖥️ | 多Agent圆桌会议决策，三维决策引擎 |
| 2 | **记忆宫殿** | 🏰 | 四域三层记忆管理，因果链映射 |
| 3 | **任务管理** | 📋 | 任务看板与追踪，智能分配 |
| 4 | **Agent管理** | 🤖 | SubAgent创建、监控、配置 |
| 5 | **技能库** | 🛠️ | 技能浏览、安装、技能市场 |
| 6 | **文档中心** | 📄 | MD文件编辑、版本管理 |
| 7 | **配置中心** | ⚙️ | 模型、License、参数配置 |
| 8 | **协同网络** | 🌐 | 局域网Agent发现与协作 |
| 9 | **对话窗口** | 💬 | DOS风格悬浮对话框 |

---

### 2.1 NEXUS 决策系统

NEXUS 是PMOS的核心决策引擎，通过多Agent圆桌会议形式进行复杂问题分析和决策。

NEXUS is the core decision engine of PMOS, using multi-agent round-table meetings for complex problem analysis and decision-making.

**四阶段圆桌流程 / Four-Stage Round Table Process:**

```
┌─────────────────────────────────────────────────────────────────┐
│  Stage 1: ICEBREAKING (破冰阶段)                                 │
│  目标: 角色自我介绍，初步形成方案框架                              │
│  Goal: Self-introduction, initial framework formation            │
├─────────────────────────────────────────────────────────────────┤
│  Stage 2: DEBATE (辩论阶段)                                      │
│  目标: 各方充分辩论，提出问题与解决方案                            │
│  Goal: Full debate, issues & solutions proposed                  │
├─────────────────────────────────────────────────────────────────┤
│  Stage 3: SELF_LOOP (自审阶段)                                   │
│  目标: Agent独自审视方案，补充完善                                │
│  Goal: Individual review, refinement                            │
├─────────────────────────────────────────────────────────────────┤
│  Stage 4: CONSENSUS (共识阶段)                                    │
│  目标: CEO最终拍板，达成决策                                      │
│  Goal: CEO final decision, consensus reached                    │
└─────────────────────────────────────────────────────────────────┘
```

**三维决策引擎 / 3D Decision Engine:**

| 维度 Dimension | 权重 Weight | 说明 Description |
|---------------|-------------|------------------|
| 意图分析 Intent Analysis | 40% | |
| Skill匹配 Skill Matching | 40% | 语义相似度 + 历史成功率 + 执行效率 |
| 记忆上下文 Memory Context | 20% | 工作/生活/知识/情感 四域记忆 |

### 2.2 记忆宫殿系统 (Memory Palace)

采用"四域三层"架构管理AI记忆，支持因果链映射和记忆思考引擎。

Memory Palace uses "Four Domains, Three Layers" architecture for AI memory management.

**四域 / Four Domains:**

| 域 Domain | 说明 Description | 示例 Example |
|-----------|-----------------|--------------|
| Work (工作域) | 工作相关记忆 | 项目进展、会议决策 |
| Life (生活域) | 日常生活记忆 | 偏好习惯、日程安排 |
| Knowledge (知识域) | 知识积累 | 技术文档、解决方案 |
| Emotion (情感域) | 情感偏好 | 用户满意度、交互风格 |

**三层 / Three Layers:**

| 层 Layer | 保留时间 Retention | 说明 Description |
|---------|-------------------|------------------|
| Short Term | 7天 | 短期会话记忆 |
| Medium Term | 90天 | 中期重要记忆 |
| Long Term | 永久 | 永久保留记忆 |

**因果链类型 / Causal Chain Types:**

- 🔗 **前置依赖链**: 完成任务的先决条件
- ⚠️ **闭坑准则链**: 历史踩坑经验总结
- 📚 **专业知识链**: 领域知识的层级关联
- 🧠 **因果推理链**: 原因→结果的推理路径

### 2.3 任务管理系统

智能任务管理，支持多维度看板和自动分配。

Intelligent task management with multi-dimensional kanban and auto-allocation.

**优先级系统 / Priority System:**

| 级别 Priority | 颜色 Color | 响应时间 Response | 场景 Scenario |
|--------------|-----------|------------------|---------------|
| **P0** | 🔴 红色 | <3秒 | @消息，即时通知 |
| **P1** | 🟠 橙色 | <30秒 | 关键词警告 |
| **P2** | 🟡 黄色 | 5-30分钟 | 普通消息 |
| **P3** | 🟢 绿色 | 不响应 | 仅记录闲聊 |

### 2.4 底层引擎切换 (Backend Switching)

PMOS 支持双底层引擎切换，满足不同场景需求：

PMOS supports dual-backend switching for different scenarios:

| 引擎 Engine | 模式 Mode | 适用场景 Use Case |
|-------------|-----------|------------------|
| **OpenClaw** | API网关 | 快速接入、依赖外部服务 |
| **WorkCow** | 自主可控 | 数据隐私、本地化部署 |

**WorkCow 核心能力 / WorkCow Core Capabilities:**

```
┌─────────────────────────────────────────────────────────────┐
│ WorkCow 六大核心模块                                         │
├─────────────────────────────────────────────────────────────┤
│ ⚡ Provider Runtime    │ 统一管理 18+ LLM 提供商            │
│ 📊 Session Manager     │ 会话管理 + 消息存储 + 谱系追踪      │
│ 🖥️ Terminal Backend    │ Local/Docker/SSH 6种后端支持       │
│ 🛠️ Tool Registry       │ 47工具 + MCP 集成                  │
│ 🔒 Sandbox Service     │ 代码执行 + 环境隔离                 │
│ ⏰ Cron Scheduler       │ 定时任务 + 自然语言解析            │
└─────────────────────────────────────────────────────────────┘
```

---

## 3. OpenClaw vs Hermes vs PMOS 对比

### 功能对比表 / Feature Comparison Table

| 功能 Feature | OpenClaw | Hermes | PMOS |
|-------------|----------|--------|------|
| **多模型支持** | ✅ | ✅ (18+) | ✅ (18+) |
| **本地部署** | ❌ 需远程 | ✅ | ✅ (WorkCow) |
| **API网关模式** | ✅ | ❌ | ✅ |
| **多Agent协同** | ⚠️ 基础 | ⚠️ 基础 | ✅ 圆桌会议 |
| **记忆系统** | ❌ | ❌ | ✅ 四域三层 |
| **任务管理** | ❌ | ❌ | ✅ 看板+分配 |
| **技能管理** | ⚠️ 基础 | ⚠️ 基础 | ✅ 市场+配置 |
| **决策引擎** | ❌ | ❌ | ✅ NEXUS |
| **因果推理** | ❌ | ❌ | ✅ 因果链 |
| **Cron调度** | ❌ | ✅ | ✅ |
| **沙箱执行** | ❌ | ✅ | ✅ (WorkCow) |
| **终端后端** | ❌ | ✅ (6种) | ✅ (6种) |
| **Web界面** | ⚠️ 简单 | ❌ | ✅ 完整PMOS |
| **像素风格UI** | ❌ | ❌ | ✅ |
| **中文支持** | ⚠️ | ⚠️ | ✅ |



#### PMOS (推荐)

| 优点 Pros | 缺点 Cons |
|-----------|-----------|
| ✅ **完整的产品体验** - 九大模块开箱即用 | ⚠️ 相对较新，生态仍在发展中 |
| ✅ **WorkCow自主可控** - 本地部署，数据不出端 | ⚠️ 完整功能需要专业版License |
| ✅ **NEXUS决策引擎** - 多Agent圆桌会议 | ⚠️ 大型团队场景待验证 |
| ✅ **四域三层记忆** - 智能记忆管理 + 因果链 | ⚠️ 部分高级功能需配置 |
| ✅ **像素风格UI** - 现代美观，易于使用 |  |
| ✅ **双模式切换** - OpenClaw/WorkCow灵活选择 |  |
| ✅ **局域网协同** - Agent自动发现与协作 |  |
| ✅ **安全机制** - 通信白名单 + 定期校验 |  |
| ✅ **中文界面** - 优秀的中文本地化 |  |

### 适用场景推荐 / Recommended Use Cases

```
┌─────────────────────────────────────────────────────────────────┐
│  推荐选择指南                                                    │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  📌 快速原型验证 / 团队协作 → OpenClaw                           │
│     Quick prototyping, team collaboration                       │
│                                                                  │
│  📌 技术深度用户 / 开发者 → Hermes                              │
│     Technical deep users, developers                            │
│                                                                  │
│  📌 企业用户 / 数据隐私 / 完整体验 → PMOS (WorkCow)            │
│     Enterprise, data privacy, complete experience               │
│                                                                  │
│  📌 多Agent协同 / 决策场景 / AI助手 → PMOS (OpenClaw)         │
│     Multi-agent collaboration, decision making, AI assistant   │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## 4. 快速开始 / Quick Start

### 4.1 初始化向导

首次使用PMOS，系统会引导完成初始化：

When first using PMOS, the system guides you through initialization:

```
步骤1: 基础数据初始化
├── ✓ 检查工作目录
├── ✓ 加载配置文件
├── ✓ 初始化数据库
└── ✓ 加载技能列表

步骤2: License 验证
├── 输入 License Key
└── 选择版本等级

步骤3: 密码设置
├── 设置管理员密码
└── 密码强度校验

步骤4: 完成初始化
└── 进入 PMOS 主界面
```

### 4.2 底层引擎选择

**方法一：通过顶部状态栏切换**

```
顶部状态栏: [OpenClaw | WorkCow] ← 点击切换
```

**方法二：通过配置中心配置**

1. 打开"配置"模块
2. 滚动到"底层引擎配置"
3. 选择目标引擎并配置参数

### 4.3 NEXUS决策流程

```
1. 打开 NEXUS 模块
2. 输入决策主题
3. 选择参与Agent
4. 启动圆桌会议
5. 观看四阶段流程
6. 获取决策产出
```

---

## 5. 配置管理 / Configuration

### 5.1 OpenClaw 配置

| 参数 Parameter | 说明 Description | 默认值 Default |
|----------------|------------------|----------------|
| Gateway URL | API网关地址 | http://localhost:8080 |
| Gateway Token | 认证令牌 | •••••••••••• |
| Timeout | 超时时间 | 30秒 |

### 5.2 WorkCow 配置

| 参数 Parameter | 说明 Description | 默认值 Default |
|----------------|------------------|----------------|
| Local Port | 本地服务端口 | 8081 |
| Provider Runtime | 模型提供商 | DashScope |
| Terminal Backend | 终端后端 | local |
| Sandbox | 沙箱服务 | 启用 |
| Cron | 定时调度 | 启用 |

### 5.3 模型配置

| 参数 Parameter | 说明 Description | 范围 Range |
|----------------|------------------|------------|
| 当前模型 | AI模型选择 | Qwen3.5-plus / GPT-4o / Claude-3 |
| Temperature | 创造性控制 | 0.0 - 1.0 |

---

## 6. 常见问题 / FAQ

### Q1: OpenClaw 和 WorkCow 有什么区别？

**A:** OpenClaw 采用API网关模式，依赖远程服务；WorkCow 是自主可控的本地引擎，数据不出端，更适合对数据隐私有要求的场景。

### Q2: 如何选择合适的底层引擎？

**A:** 
- 快速验证概念 → OpenClaw
- 企业级部署 → WorkCow
- 数据隐私敏感 → WorkCow
- 追求低延迟 → WorkCow

### Q3: NEXUS 决策系统支持哪些场景？

**A:** 产品需求分析、技术方案评审、商业决策讨论、代码Review、团队协作规划等。

### Q4: 记忆宫殿的因果链有什么用？

**A:** 因果链可以帮助AI理解知识点之间的关系，在问题分析时沿因果链推理，提供更准确的答案。

### Q5: 如何导入已有任务？

**A:** 在NEXUS决策完成后，点击"导入任务"按钮，产出的任务会自动同步到任务管理系统。

---

## 附录 / Appendix

### A. 快捷键 / Keyboard Shortcuts

| 快捷键 Shortcut | 功能 Function |
|-----------------|---------------|
| `Ctrl + 1-9` | 切换模块 |
| `Ctrl + Enter` | 发送消息 |
| `Esc` | 关闭弹窗 |

### B. 版本信息 / Version Info

| 项目 Item | 内容 Content |
|-----------|--------------|
| PMOS版本 | 3.34 |
| 发布日期 | 2026-04-23 |
| 底层引擎 | OpenClaw / WorkCow |


---

**© 2026 PMOS. All rights reserved.**  
**Made with ❤️ for AI Collaboration**
