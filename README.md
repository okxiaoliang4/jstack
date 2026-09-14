# Jstack

This repository is a private Agent Plugins package containing the reusable skills from `~/.agents/skills`.

## Layout

- `plugin.json` — Agent Plugins v1 manifest.
- `.claude-plugin/plugin.json` — Claude Code plugin manifest.
- `.claude-plugin/marketplace.json` — Claude Code marketplace manifest, so the repository can be added as a marketplace directly.
- `skills/<skill-name>/SKILL.md` — discoverable Agent Skills and their bundled references, scripts, and assets.

There is no `mcp.json` because this package currently provides skills only.

## Install in Claude Code

```
/plugin marketplace add okxiaoliang4/jstack
/plugin install jstack@jelf-agent-plugins
```

Claude Code discovers `skills/` at the plugin root, so all skills become available as
`jstack:<skill-name>` after installation.

## Source snapshot

The initial snapshot was imported from `/Users/jelf/.agents/skills`. Home Manager/Nix symlinks were materialized as regular files so the package is self-contained and satisfies the Agent Plugins path-containment rules. Local `.git` history, `.DS_Store`, and `*.hm-backup-*` backup artifacts were intentionally left out.

The source directory is managed by other tooling, so update this repository by reviewing and importing a fresh snapshot rather than replacing the source directory with a checkout.

## Specification

The package targets Agent Plugins Specification 1.0.0:

<https://agent-plugins.org/specification>
