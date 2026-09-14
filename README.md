# Jstack

A personal collection of reusable agent skills, packaged as a plugin for both Claude Code and Codex.

The 55 skills under `skills/` cover planning, implementation, review, writing, and design
workflows. Read `skills/<name>/SKILL.md` to see what each one does.

## Install

### Claude Code

```
/plugin marketplace add okxiaoliang4/jstack
/plugin install jstack@jelf-agent-plugins
```

Skills become available as `jstack:<skill-name>`.

### Codex

```
codex plugin marketplace add okxiaoliang4/jstack
codex plugin add jstack@jelf-agent-plugins
```

Both clients discover `skills/` at the plugin root, and both resolve the plugin from the
marketplace named `jelf-agent-plugins`, so the install id is `jstack@jelf-agent-plugins`
either way.

## Layout

| Path | Purpose |
| --- | --- |
| `plugin.json` | Agent Plugins v1 manifest |
| `.claude-plugin/plugin.json` | Claude Code plugin manifest |
| `.claude-plugin/marketplace.json` | Claude Code marketplace manifest |
| `.codex-plugin/plugin.json` | Codex plugin manifest |
| `.agents/plugins/marketplace.json` | Codex marketplace manifest |
| `skills/<name>/SKILL.md` | A skill, plus its bundled references, scripts, and assets |

There is no `mcp.json` because this package provides skills only.

## Specification

Targets [Agent Plugins Specification 1.0.0](https://agent-plugins.org/specification).
