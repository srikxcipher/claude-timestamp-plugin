# claude-timestamp-plugin

A Claude Code plugin that adds timestamps to every conversation — visible in your terminal and saved to an audit log.

## What it does

- Shows `⏱  [2026-04-20 14:32:05]` in the terminal when you submit a prompt
- Shows `⏱  [2026-04-20 14:36:00]` after Claude finishes responding
- Appends both events to `~/.claude/timestamp-audit.log` for persistent audit trail
- Zero extra token consumption for the audit log

## Install

```bash
claude plugin marketplace add srikxcipher/claude-timestamp-plugin
claude plugin install chat-timestamp
```

Restart Claude Code. That's it.

## Uninstall

```bash
claude plugin uninstall chat-timestamp
```

## Audit log

Entries are appended to `~/.claude/timestamp-audit.log`:

```
[2026-04-20 14:32:05] User prompt submitted
[2026-04-20 14:36:00] Claude response completed
[2026-04-20 14:37:10] User prompt submitted
[2026-04-20 14:38:45] Claude response completed
```

Tail it live during a session:

```bash
tail -f ~/.claude/timestamp-audit.log
```

## Requirements

- Claude Code v2.0+
- macOS or Linux (Windows supported via Git Bash)
