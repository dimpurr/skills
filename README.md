# skills

Agent skills by [dimpurr](https://github.com/dimpurr). Works with Claude Code, Cursor, Codex, Windsurf, Grok Bot and [the other agents supported by skills.sh](https://skills.sh/).

## Available Skills

| Skill | Description |
|-------|-------------|
| [grok-bot-gateway](skills/grok-bot-gateway/) | One entry point for both sides of a webhook-triggered Grok Bot gateway: callers (Claude Code, Codex, scripts) list, read and message a Grok Bot team; hosts (a Grok Bot account) set up the gateway Bot. Detects your role and guides you. `npx skills add dimpurr/skills --skill grok-bot-gateway` · _updated 2026-10-03_ |

## Quick Install

Uses the [skills](https://github.com/vercel-labs/skills) CLI ([skills.sh](https://skills.sh/)).

```bash
# List the skills in this repo
npx skills add dimpurr/skills --list

# Install a specific skill
npx skills add dimpurr/skills --skill grok-bot-gateway

# Install all skills
npx skills add dimpurr/skills --all

# Global install (available across all projects), no prompts
npx skills add dimpurr/skills --skill grok-bot-gateway -g -y
```

## Manual Install

Each skill is a directory under `skills/` with a `SKILL.md` file. Copy the whole skill directory (scripts and other files included) into your agent's skill folder:

- **Claude Code**: `.claude/skills/` (global: `~/.claude/skills/`)
- **Cursor, Codex and most others**: `.agents/skills/`
- **Windsurf**: `.windsurf/skills/`
- **Grok Bot**: hand the skill's `SKILL.md` to a Bot and ask it to save it as a skill. The Bot keeps it in your account's shared skill library. If the skill ships scripts, give the Bot those files too.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the per-skill folder convention.

## See also

- [iopho-skills](https://github.com/iopho-team/iopho-skills): Agent skills for iopho products (reading, notes, video production).

## License

[Apache-2.0](LICENSE). Copyright 2026 dimpurr <dimpurr@live.com>.
