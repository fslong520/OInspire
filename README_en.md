# 🧑‍🏫 OInspire

> An AI-powered Olympiad in Informatics (OI) coach — heuristic teaching, patient guidance, and a memory system that grows with every conversation.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Powered by](https://img.shields.io/badge/powered%20by-QwenPaw-7c3aed.svg)](https://qwenpaw.com)

[中文版](README.md)

---

## Table of Contents

- [What is OInspire](#what-is-oinspire)
- [Core Features](#core-features)
- [Quick Start](#quick-start)
- [Project Structure](#project-structure)
- [Knowledge Coverage](#knowledge-coverage)
- [Memory System](#memory-system)
- [Contributing](#contributing)
- [License](#license)

---

## What is OInspire

**OInspire** (OI + Inspire) is not a Q&A bot. It's a **warm, patient competition coach** that lives inside the [QwenPaw](https://qwenpaw.com) multi-agent framework.

Instead of handing out answers, it asks the right questions. Instead of one-size-fits-all, it builds a deep understanding of each student over time — from the first "hello" to the 50th conversation where it can already predict where the student will get stuck.

> _Every child is a potential champion. All we need to do is light the fire._

---

## Core Features

### 🎯 Heuristic Teaching
- Guides students to discover solutions through questioning, not direct answers
- Breaks complex problems into small, confidence-building steps
- Uses analogies and real-world examples to explain abstract algorithms

### 📈 Memory That Grows With You
A built-in tracking system that auto-updates after every session:

| File | Purpose |
|------|---------|
| `profile.md` | Student portrait: personality, style, strengths & weaknesses |
| `knowledge_matrix.md` | Knowledge mastery matrix: per-topic proficiency tracking |
| `templates.md` | Algorithm templates: fluency, can they write it blindfolded? |
| `error_log.md` | Error log: failure patterns, high-frequency mistakes |
| `contest_log.md` | Contest records: scores, mindset, upsolving progress |

**Cumulative effect:** 1st conversation → knows your name and goal. 50th conversation → predicts where you'll get stuck.

### 📋 Personalized Problem Sets
- Generates customized problem sets based on student level, target contest, and available time
- Four stages: Beginner → Intermediate → Advanced → Sprint
- Supports post-contest upsolving plans and template drill schedules

### 🔥 Competition Strategy
- **Upsolving is king:** Problems not solved after the contest must be revisited
- **Template mastery:** Every template must be typed 3+ times from memory
- **Deliberate practice:** Consistency beats intensity — 1h daily > 10h weekend

---

## Quick Start

### Prerequisites

- [QwenPaw](https://qwenpaw.com) installed and configured
- Python 3.10+

### Setup

1. **Clone the repository**

```bash
git clone git@github.com:fslong520/OInspire.git
cd OInspire
```

2. **Deploy to QwenPaw**
   - Locate your QwenPaw default workspace directory.
   - Copy the core files (`AGENTS.md`, `SOUL.md`, `PROFILE.md`, `memory/`, `skills/`) into it.
   - **Overwrite** existing files if prompted.

3. **Start**
   - Launch QwenPaw to start using the coach.

---

## Project Structure

```
OInspire/
├── AGENTS.md                  # Core behavior rules & workflow
├── SOUL.md                    # Teaching philosophy, style, quotes
├── PROFILE.md                 # Agent identity & user profile
├── MEMORY.md                  # Tool settings & runtime notes
├── README.md                  # Chinese README (default)
├── README_en.md               # English README
├── LICENSE                    # MIT License
├── .gitignore                 # Whitelist-only git ignore
│
├── memory/
│   └── student/               # Student memory templates (auto-updated)
│       ├── profile.md
│       ├── knowledge_matrix.md
│       ├── templates.md
│       ├── error_log.md
│       ├── contest_log.md
│       ├── conversation_log.md
│       └── INDEX.md
│
└── skills/
    ├── problem_set_generator/ # Personalized problem set & plan generator
    │   ├── SKILL.md
    │   ├── knowledge_map.md
    │   └── templates/
    │       ├── beginner.md
    │       ├── intermediate.md
    │       ├── advanced.md
    │       └── sprint.md
    └── ...                    # Additional skills
```

---

## Knowledge Coverage

| Stage | Core Topics |
|-------|------------|
| 🟢 Beginner | Variables, loops, conditions, arrays, strings, basic functions |
| 🟡 Foundation | Sorting, binary search, stacks/queues, greedy, simple DFS/BFS, linear DP |
| 🟠 Intermediate | Graph theory, shortest path, MST, knapsack DP, interval/tree DP, DSU |
| 🔴 Advanced | Advanced DP, SCC, segment trees, KMP, number theory |
| ⚫ Sprint | Network flow, suffix automata, balanced trees, computational geometry, game theory |

---

## Memory System

OInspire maintains a tiered memory architecture under `memory/student/`. After **every** coaching session, the agent automatically updates:

- **Profile** — new preferences, communication style observations
- **Knowledge Matrix** — which topics improved, which need review
- **Error Log** — mistakes made, patterns spotted, review schedule
- **Contest Log** — performance, emotional state, upsolving status
- **Conversation Log** — session summary, next steps

This ensures continuity across sessions, even if the agent is restarted.

---

## Contributing

Contributions are welcome!

- **Bug reports & feature requests** → open an [Issue](https://github.com/fslong520/OInspire/issues)
- **Code & documentation** → submit a [Pull Request](https://github.com/fslong520/OInspire/pulls)
- **Ideas & discussions** → use [Discussions](https://github.com/fslong520/OInspire/discussions)

---

## License

This project is licensed under the [MIT License](LICENSE).

---

<p align="center">
  <sub>Not afraid you can't do it — afraid you won't try.</sub>
</p>
