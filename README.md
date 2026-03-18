# context-handoff

A local AgentSkill for OpenClaw that saves and restores conversation handoff notes and project summaries using plain markdown files.

## What it does

- Save session-level handoff context into `handoffs/sessions/<slot>.md`
- Restore session context by slot name
- List saved session slots
- Save project summaries into `projects/<project-name>.md`
- Restore project summaries by project name
- List project summaries
- Sort listed results by **last updated time** so the most recently used items appear first

## Why this skill exists

When you switch accounts, reset sessions, or move across chat threads, useful working context gets lost easily. This skill makes context handoff explicit and file-based instead of relying on chat history surviving forever.

## Trigger examples

- 保存当前上下文
- 保存会话摘要
- 恢复上下文
- 恢复 oauth-switch 项目摘要
- 列出已保存摘要
- 按更新时间排序列出项目摘要
- save session context
- restore project summary
- list project summaries
- sort by updated time

## Install locally

Clone or copy this repo, then place the skill folder under your local skills directory, for example:

```bash
mkdir -p ~/.agents/skills
cp -R context-handoff ~/.agents/skills/
```

## Publish to ClawHub

After logging in with the ClawHub CLI:

```bash
clawhub publish ./context-handoff \
  --slug context-handoff \
  --name "Context Handoff" \
  --version 0.1.0 \
  --changelog "Initial public release with updated-time sorting"
```

Users can then search and install it with:

```bash
clawhub search "context handoff"
clawhub install context-handoff
```

## Repository layout

```text
context-handoff-skill/
├── README.md
└── context-handoff/
    └── SKILL.md
```
