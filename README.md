# 继承者（Successor）— 智能体接替技能

[中文](README.md) | [English](README_en.md)

---

## 概述

**继承者（Successor）** 是一个 AI Agent 接替与任务延续技能，专为解决智能体通信上限问题而设计。当智能体达到对话上限时，继承者自动承接上下文、任务状态、记忆系统和文件/项目文件，实现无缝工作衔接。

## 核心功能

- **上下文迁移** — 自动读取并整合对话历史、决策过程
- **任务状态衔接** — 识别当前任务进展，分析未完成项
- **记忆接管** — 读取 MEMORY.md 和 daily notes，继承长期记忆
- **文件/项目接管** — 识别工作区文件，了解项目结构与状态
- **断点续传** — 基于已有信息，无缝衔接工作，不遗漏任何关键上下文

## 安装

### SkillHub（推荐）

`ash
npx skills add richard3153/successor-skill@successor
`

### 手动安装

将 skills/successor/ 目录复制到你的 OpenClaw skills 目录即可。

## 使用场景

- 原智能体报告「达到沟通上限」「即将结束会话」
- 需要在新会话中延续之前的复杂任务
- 多人协作时，新智能体需要接手前任的工作

## 文件结构

`
successor-skill/
└── skills/
    └── successor/
        ├── SKILL.md                    # 核心技能定义
        └── references/
            ├── 接替状态评估.md          # 详细的评估框架
            ├── 上下文文件索引.md        # 上下文文件说明
            └── 文件与项目识别.md        # 文件识别指南
`

## 关键词

接替、继承、延续、上下文迁移、任务续接、记忆交接、文件接管、项目延续、successor、inherit、continue

## 开源协议

MIT License — 详见 [LICENSE](LICENSE) 文件

## 作者

richard3153

---

*如果你觉得这个技能有用，欢迎 Star ⭐ 和分享！*