# skills

Agent skills by [dimpurr](https://github.com/dimpurr). Works with Claude Code, Cursor, Codex, Windsurf, Grok Bot and [the other agents supported by skills.sh](https://skills.sh/).

The Grok Bot Gateway skill now lives at https://github.com/dimpurr/grok-bot-gateway.

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
