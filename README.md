# 🧑‍🏫 OInspire

> 一个基于 QwenPaw 的 AI 信息学竞赛教练智能体 —— 启发式教学，耐心引导，越用越懂孩子。

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Powered by](https://img.shields.io/badge/powered%20by-QwenPaw-7c3aed.svg)](https://qwenpaw.com)

[English Version](README_en.md)

---

## 目录

- [OInspire 是什么](#oinspire-是什么)
- [核心特色](#核心特色)
- [快速开始](#快速开始)
- [项目结构](#项目结构)
- [知识点覆盖](#知识点覆盖)
- [记忆系统](#记忆系统)
- [参与贡献](#参与贡献)
- [开源协议](#开源协议)

---

## OInspire 是什么

**OInspire**（OI + Inspire）不是一个问答机器人。它是一个**有温度的竞赛教练**，运行在 [QwenPaw](https://qwenpaw.com) 多智能体框架中。

它不会直接抛出答案，而是用问题引导学生自己找到解法；它不会千篇一律，而是在每一次对话中不断了解这个孩子——从第一次打招呼，到第 50 次对话时已经能预判学生会在哪里卡壳。

> _每个孩子都是潜在的冠军，我们需要做的就是点燃他们心中的火。_

---

## 核心特色

### 🎯 启发式教学
- 不给答案，用提问引导学生自己发现解法
- 把复杂问题拆成小步骤，让每个小成功都积累信心
- 善用类比和生活例子解释抽象的算法概念

### 📈 越用越懂孩子
内置完整的记忆追踪系统，每次会话后自动更新：

| 文件 | 用途 |
|------|------|
| `profile.md` | 学生画像：性格、学习风格、优势与薄弱点 |
| `knowledge_matrix.md` | 知识掌握矩阵：每个知识点的状态追踪 |
| `templates.md` | 算法模板库：模板熟练度、能否闭眼写出 |
| `error_log.md` | 错题本：错误原因分类、高频模式识别 |
| `contest_log.md` | 比赛记录：成绩、心态、赛后 upsolving 进度 |

**累积效应：** 第 1 次知道名字和目标 → 第 50 次能预判会卡在什么题上。

### 📋 智能题单与训练计划
- 根据学生水平、目标比赛、可用时间，生成个性化题单
- 入门 / 基础 / 提高 / 冲刺四阶段训练模板
- 支持 Upsolving（赛后补题）计划和模板训练计划

### 🔥 比赛策略与训练方法论
- **Upsolving 最重要：** 做过的题不复盘，等于白做；赛后补题，等于白比
- **模板建设：** 每个模板亲手敲过 3 遍以上才算数
- **刻意练习：** Consistency beats intensity —— 每天 1 小时 > 周末突击 10 小时

---

## 快速开始

### 前置要求

- 已安装 [QwenPaw](https://qwenpaw.com) 或兼容的多智能体框架
- Python 3.10+

### 使用方式

1. **克隆仓库**

```bash
git clone git@github.com:fslong520/OInspire.git
cd OInspire
```

2. **部署到 QwenPaw**
   - 找到你的 QwenPaw 默认工作区目录。
   - 将本项目的核心文件（`AGENTS.md`, `SOUL.md`, `PROFILE.md`, `memory/`, `skills/`）复制进去。
   - 如果已有同名文件，请**替换**它们。

3. **启动**
   - 启动 QwenPaw，即可开始使用教练智能体。

---

## 项目结构

```
OInspire/
├── AGENTS.md                  # 核心行为配置
├── SOUL.md                    # 教练灵魂（教学理念、风格指引）
├── PROFILE.md                 # 身份与用户资料模板
├── MEMORY.md                  # 记忆配置
├── README.md                  # 中文 README（默认）
├── README_en.md               # English README
├── LICENSE                    # MIT License
├── .gitignore                 # 白名单模式 gitignore
│
├── memory/
│   └── student/               # 学生记忆模板（会话后自动更新）
│       ├── profile.md
│       ├── knowledge_matrix.md
│       ├── templates.md
│       ├── error_log.md
│       ├── contest_log.md
│       ├── conversation_log.md
│       └── INDEX.md
│
└── skills/
    ├── problem_set_generator/ # 题单与训练计划生成器
    │   ├── SKILL.md
    │   ├── knowledge_map.md
    │   └── templates/
    │       ├── beginner.md
    │       ├── intermediate.md
    │       ├── advanced.md
    │       └── sprint.md
    └── ...                    # 其他 Skills
```

---

## 知识点覆盖

| 阶段 | 核心内容 |
|------|---------|
| 🟢 入门 | 变量、循环、条件、数组、字符串、基础函数 |
| 🟡 基础 | 排序、二分、栈/队列、贪心、简单搜索、线性 DP |
| 🟠 提高 | 图论、最短路、MST、背包 DP、区间/树形 DP、并查集 |
| 🔴 进阶 | 高级 DP、强连通分量、线段树、KMP、数论 |
| ⚫ 冲刺 | 网络流、后缀自动机、平衡树、计算几何、博弈论 |

---

## 记忆系统

OInspire 在 `memory/student/` 下维护分层记忆架构。**每次辅导会话结束后**，教练智能体会自动更新：

- **学生画像** — 新偏好、沟通风格观察
- **知识矩阵** — 哪些知识点进步了，哪些需要复习
- **错题本** — 犯过的错误、发现的规律、复习排期
- **比赛记录** — 成绩表现、心态状态、upsolving 进度
- **对话日志** — 会话摘要、下一步计划

这确保了跨会话的连续性，即使智能体重启也不会丢失上下文。

---

## 参与贡献

欢迎提交 Issue 和 Pull Request！

- **报告 Bug 或提出功能建议** → 开 [Issue](https://github.com/fslong520/OInspire/issues)
- **贡献代码或文档** → 开 [Pull Request](https://github.com/fslong520/OInspire/pulls)
- **想法与交流** → 使用 [Discussions](https://github.com/fslong520/OInspire/discussions)

---

## 开源协议

本项目采用 [MIT License](LICENSE) 开源协议。

---

<p align="center">
  <em>不怕你不会，就怕你不敢试。</em>
</p>
