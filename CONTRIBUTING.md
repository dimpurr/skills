# Contributing

## Skill layout

One folder per skill, following the [Agent Skills specification](https://agentskills.io/specification) and the layout the [skills CLI](https://github.com/vercel-labs/skills) discovers:

```
skills/<name>/
├── SKILL.md        # required: YAML frontmatter + instructions
├── scripts/        # optional: executables the skill runs (keep them chmod +x)
├── references/     # optional: longer docs loaded on demand
├── assets/         # optional: templates, data files
└── contracts/      # optional: JSON Schemas or other interface definitions
```

## `SKILL.md` frontmatter

```yaml
---
name: my-skill            # required; must equal the folder name
description: What it does and when to use it.   # required; max 1024 chars
license: Apache-2.0       # matches this repo's LICENSE
compatibility: Runtime needs (optional; max 500 chars)
metadata:                 # optional string-to-string map
  author: dimpurr
  version: "0.1.0"
---
```

- `name`: 1-64 chars, lowercase letters, digits and single hyphens; no leading or trailing hyphen.
- Refer to files with paths relative to the skill folder (e.g. `scripts/tool`), one level deep.
- Keep `SKILL.md` under about 500 lines; move long reference material into `references/`.

## Rules

- **No secrets or personal data.** No keys, tokens, webhook URLs, IP addresses, host names, account or agent ids, or personal paths. Use placeholders and environment variables, and document the defaults.
- Scripts read configuration from environment variables and never print secrets.
- Test scripts locally (against a mock where a live service would cost money or touch real accounts) before opening a PR.
- Add the skill to the table in `README.md` with a one-line description and its install command.
- Check that the CLI finds it: `npx skills add . --list`.
