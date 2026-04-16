# 继承者 (Successor) - 智能体接替与任务延续 Skill

[English](README.md) | 中文

## 概述

**继承者** (Successor) 是一个专为 AI Agent 设计的智能接替与任务延续 Skill。当智能体达到沟通上限、会话重置、或需要新智能体接替工作时，确保上下文、任务、记忆、文件的完整传承。

## 使用场景

### 1. 智能体沟通上限接替
- 原智能体提示"沟通上限"、"即将重置"
- 新智能体启动，需要继承前任所有工作状态
- 上下文完整迁移，无信息丢失

### 2. 跨会话任务延续
- 用户说"继续上次的任务"、"接替之前的工作"
- 长任务中断后恢复执行
- 多阶段工作流的断点续传

### 3. 记忆系统接管
- 长期记忆 (MEMORY.md) 无缝衔接
- 短期记忆 (memory/YYYY-MM-DD.md) 完整读取
- 用户偏好、关键决策、待办事项全面继承

### 4. 文件与项目接管
- 扫描并识别前任创建的所有文件与目录
- 理解项目结构，评估项目状态
- 确认关键文件位置和项目进度

## 核心功能

| 功能 | 说明 |
|------|------|
| 上下文迁移 | 读取 SOUL.md, IDENTITY.md, USER.md, MEMORY.md |
| 任务状态衔接 | 识别进行中的任务，待办事项 |
| 记忆接管 | 长期与短期记忆文件无缝衔接 |
| 文件/项目接管 | 扫描工作区，识别所有创建的文件和项目 |
| 断点续传 | 从中断处继续，无需重新摸索 |

## 触发关键词

接替、继承、延续、上下文迁移、任务续接、记忆交接、文件接管、项目延续

## 安装

### 通过 SkillHub 安装（推荐）

```bash
skillhub install successor
```

### 手动安装

1. 克隆仓库到本地：
```bash
git clone https://github.com/your-username/successor-skill.git
```

2. 将 `successor` 目录复制到 OpenClaw skills 目录：
```bash
# Windows
copy successor %USERPROFILE%\.qclaw\skills\

# macOS / Linux
cp -r successor ~/.qclaw/skills/
```

## 使用方法

### 基础接替

当需要接替前任智能体工作时：

1. **自动触发**：提及"接替"、"继续"、"继承"等关键词时自动激活
2. **读取上下文**：自动扫描并读取相关上下文文件
3. **构建摘要**：向用户确认接替状态

### 接替工作流

```
1. 读取上下文文件
   ├── SOUL.md          → 智能体身份与风格
   ├── IDENTITY.md      → 名称、经历、配置
   ├── USER.md          → 用户信息与偏好
   ├── MEMORY.md        → 长期记忆
   └── memory/          → 近期工作记录

2. 扫描项目文件
   ├── 工作区文件扫描
   ├── 项目结构识别
   └── 进行中项目确认

3. 构建接替摘要
   ├── 用户信息确认
   ├── 当前任务状态
   ├── 识别项目列表
   └── 待办事项整理

4. 任务延续
   ├── 确认文件修改进度
   ├── 检查外部操作状态
   └── 继续执行任务
```

## 目录结构

```
successor/
├── SKILL.md                         # 核心技能定义
└── references/
    ├── 接替状态评估.md               # 状态分级参考
    ├── 上下文文件索引.md             # 文件读取指南
    └── 文件与项目识别.md             # 项目识别与检查
```

## 状态评估

### 🟢 完整接替 (Green)
- 所有上下文文件存在且最新
- 任务状态清晰，无悬空操作
- 用户偏好已记录
- 项目文件完整

### 🟡 部分接替 (Yellow)
- 部分文件缺失或过时
- 任务状态不明
- 需要用户确认

### 🔴 断档接替 (Red)
- 关键文件全部缺失
- 无历史记录
- 需要重新建立上下文

## 与其他 Skills 配合

- **memory 系统**：依赖 memory/ 目录进行记忆读取
- **qclaw-cron-skill**：检查定时任务状态
- **qclaw-text-file**：确保文件编码正确

## 贡献

欢迎提交 Issue 和 Pull Request！

## 许可证

MIT License

---

## English Version

### Overview

**Successor** is a skill designed for AI Agents to handle succession and task continuity. When an agent reaches communication limits, session resets, or needs a new agent to take over, it ensures complete context, task, memory, and file inheritance.

### Key Features

- Context migration from previous sessions
- Task state continuity
- Memory system takeover
- File and project handover
- Seamless task resumption

### Installation

```bash
skillhub install successor
```

### Usage

Simply mention keywords like "接替" (take over), "继续" (continue), or "继承" (inherit) to trigger the skill. It will automatically:
1. Read relevant context files
2. Scan for project files
3. Build a succession summary
4. Confirm with the user

### License

MIT License
