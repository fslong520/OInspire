# 🧑‍🏫 OInspire

> OI + Inspire — 一个基于 CoPaw 的 AI 信息学竞赛教练智能体

**OInspire** 不是一个普通的问答机器人。它是一个**有温度的竞赛教练**，擅长启发式教学、循循善诱，并能在与学生的每一次对话中不断了解这个孩子，越用越懂。

---

## ✨ 核心特色

### 🎯 启发式教学
- 不直接给答案，而是用问题引导学生自己找到解法
- 把复杂问题拆成小步骤，让学生在每个小成功中积累信心
- 善用类比和生活例子解释抽象的算法概念

### 📈 越用越懂孩子
内置完整的记忆追踪系统：

| 模块 | 用途 |
|------|------|
| `profile.md` | 学生画像：性格、学习风格、优势薄弱点 |
| `knowledge_matrix.md` | 知识掌握矩阵：每个知识点的状态追踪 |
| `templates.md` | 算法模板库：模板熟练度、能否闭眼写出 |
| `error_log.md` | 错题本：错误原因分类、高频模式识别 |
| `contest_log.md` | 比赛记录：成绩、心态、赛后 upsolving 进度 |

**累积效应：** 第 1 次对话知道名字和目标 → 第 50 次对话能预判学生会卡在什么题上。

### 📋 智能题单与训练计划
- 根据学生水平、目标比赛、可用时间，一键生成个性化题单
- 包含入门/基础/提高/冲刺四个阶段的训练模板
- 支持 Upsolving（赛后补题）计划和模板训练计划

### 🔥 比赛策略与训练方法论
- Upsolving 方法论：赛后补题是最重要的提升方式
- 模板库建设：每个模板亲手敲过 3 遍才算数
- 刻意练习原则：Consistency beats intensity

### 🎭 风趣幽默，金句不断
- 即兴创造金句，不背稿
- 源于场景，带点哲理，把编程和人生的道理打通
- 善意调侃，点到为止

---

## 🚀 快速开始

### 前置要求

- 已安装 [CoPaw](https://copaw.dev) 或兼容的多智能体框架
- 支持 Python 3.10+

### 使用方式

1. 将本项目作为 Workspace 加载到 CoPaw
2. 配置 `agent.json`（包含模型、渠道等）
3. 启动后即可与学生对话

```bash
# clone 项目
git clone git@github.com:fslong520/OInspire.git

# 配置 CoPaw 指向此 workspace 目录
# 具体步骤请参考 CoPaw 官方文档
```

---

## 📂 项目结构

```
OInspire/
├── AGENTS.md                  # 核心行为配置
├── SOUL.md                    # 教练灵魂（教学理念、风格指引）
├── PROFILE.md                 # 身份与用户资料模板
├── MEMORY.md                  # 记忆配置
├── .gitignore                 # 白名单模式 gitignore
├── memory/
│   └── student/
│       ├── profile.md         # 学生画像
│       ├── knowledge_matrix.md# 知识掌握矩阵
│       ├── templates.md       # 算法模板库
│       ├── error_log.md       # 错题本
│       ├── contest_log.md     # 比赛记录
│       ├── conversation_log.md# 对话记录
│       └── INDEX.md           # 记忆系统说明
└── skills/
    ├── problem_set_generator/ # 题单与训练计划生成器
    │   ├── SKILL.md           # 使用说明
    │   ├── knowledge_map.md   # 完整知识点地图
    │   └── templates/         # 各阶段训练模板
    ├── 搬题姬/                # 题目创作辅助
    ├── 备课/                  # 备课辅助
    ├── 命题工坊/              # 命题工具
    ├── 墨池/                  # 知识库与学习追踪
    └── ...                    # 其他内置 Skills
```

---

## 🗺️ 知识点覆盖

从入门到冲刺，完整覆盖信息学竞赛知识体系：

| 阶段 | 核心内容 |
|------|---------|
| 🟢 入门 | 变量、循环、条件、数组、字符串、基础函数 |
| 🟡 基础 | 排序、二分、栈/队列、贪心、简单搜索、线性 DP |
| 🟠 提高 | 图论、最短路、MST、背包 DP、区间/树形 DP、并查集 |
| 🔴 进阶 | 高级 DP、强连通分量、线段树、KMP、数论 |
| ⚫ 冲刺 | 网络流、后缀自动机、平衡树、计算几何、博弈论 |

---

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

- 报告 Bug 或提出功能建议 → 开 Issue
- 贡献代码或文档 → 开 PR
- 分享使用心得 → Discussion

---

## 📄 开源协议

本项目采用 [MIT License](LICENSE) 开源协议。

---

## 💬 联系方式

- **GitHub:** [fslong520/OInspire](https://github.com/fslong520/OInspire)
- **CoPaw:** [copaw.dev](https://copaw.dev)

---

> _每个孩子都是潜在的冠军，我们需要做的就是点燃他们心中的火。_
