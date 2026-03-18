# context-handoff

一个给 OpenClaw 用的本地 AgentSkill，用纯 Markdown 文件保存和恢复会话交接信息与项目摘要。

A local AgentSkill for OpenClaw that saves and restores conversation handoff notes and project summaries using plain markdown files.

---

## 中文说明

### 它能做什么

- 把会话级上下文保存到 `handoffs/sessions/<slot>.md`
- 按槽位名恢复会话上下文
- 列出已保存的会话槽位
- 把项目摘要保存到 `projects/<project-name>.md`
- 按项目名恢复项目摘要
- 列出已保存的项目摘要
- 列表按**最后更新时间**排序，最近更新的排最前

### 为什么需要这个 skill

当你切换账号、重置 session、或者换聊天线程时，工作上下文很容易丢。这个 skill 把“上下文交接”做成显式、可落盘、可恢复的文件化流程，而不是赌聊天记录永远都在。

### 触发示例

- 保存当前上下文
- 保存会话摘要
- 恢复上下文
- 恢复 oauth-switch 项目摘要
- 列出已保存摘要
- 按更新时间排序列出项目摘要

### 本地安装

把仓库里的 `context-handoff` 文件夹放到本地 skills 目录，例如：

```bash
mkdir -p ~/.agents/skills
cp -R context-handoff ~/.agents/skills/
```

### 发布到 ClawHub

```bash
clawhub publish ./context-handoff \
  --slug context-handoff \
  --name "Context Handoff" \
  --version 0.1.0 \
  --changelog "Initial public release with updated-time sorting"
```

### 用户搜索和安装

```bash
clawhub search "context handoff"
clawhub install context-handoff
```

---

## English

### What it does

- Save session-level handoff context into `handoffs/sessions/<slot>.md`
- Restore session context by slot name
- List saved session slots
- Save project summaries into `projects/<project-name>.md`
- Restore project summaries by project name
- List project summaries
- Sort listed results by **last updated time** so the most recently used items appear first

### Why this skill exists

When you switch accounts, reset sessions, or move across chat threads, useful working context gets lost easily. This skill makes context handoff explicit and file-based instead of relying on chat history surviving forever.

### Trigger examples

- save session context
- restore project summary
- list project summaries
- sort by updated time

### Install locally

Clone or copy this repo, then place the skill folder under your local skills directory, for example:

```bash
mkdir -p ~/.agents/skills
cp -R context-handoff ~/.agents/skills/
```

### Publish to ClawHub

```bash
clawhub publish ./context-handoff \
  --slug context-handoff \
  --name "Context Handoff" \
  --version 0.1.0 \
  --changelog "Initial public release with updated-time sorting"
```

### Search and install

```bash
clawhub search "context handoff"
clawhub install context-handoff
```

---

## Repository layout

```text
context-handoff-skill/
├── README.md
└── context-handoff/
    └── SKILL.md
```
