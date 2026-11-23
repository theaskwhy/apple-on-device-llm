# Apple On-Device LLM — an Agent Skill by The Ask Why Company

Run Apple's free on-device language model from the terminal.

**When it's used:** use when you want to run Apple's free on-device language model (Foundation Models framework, Apple Intelligence Macs) from the command line for short private text tasks such as hooks, captions or summaries.

Read the skill: [skills/apple-on-device-llm/SKILL.md](skills/apple-on-device-llm/SKILL.md)

Works with Claude (Claude Code, Claude.ai) and any tool that reads the open [Agent Skills](https://agentskills.io) `SKILL.md` format.

## Install in Claude
**Claude Code:**
```
/plugin marketplace add theaskwhy/apple-on-device-llm
/plugin install apple-on-device-llm@apple-on-device-llm
```
Or from the full catalogue: `/plugin marketplace add theaskwhy/skills` then `/plugin install apple-on-device-llm@theaskwhy`.

**Manual:** copy `skills/apple-on-device-llm/` into `~/.claude/skills/` (personal) or `.claude/skills/` (project).

**Claude.ai:** zip the `skills/apple-on-device-llm` folder and upload it under Settings → Capabilities → Skills.

## Use it with any AI agent
This skill uses the open **Agent Skills** standard (`SKILL.md`), so the same file works in Claude Code, OpenAI Codex, Cursor, Gemini CLI, GitHub Copilot, Windsurf, Antigravity, OpenCode, Goose and many more.

**Quickest (any supported agent):** the open-source `skills` installer detects your tools and installs for them:
```
npx skills add theaskwhy/apple-on-device-llm
```

**Manual:** copy `skills/apple-on-device-llm/` into your tool's skills folder:

| Tool | Personal (all projects) | One project |
|---|---|---|
| Claude Code | `~/.claude/skills/` | `.claude/skills/` |
| OpenAI Codex | `~/.codex/skills/` | `.agents/skills/` |
| Cursor | `~/.cursor/skills/` | `.cursor/skills/` |
| Gemini CLI / Antigravity | `~/.gemini/skills/` | `.gemini/skills/` |
| GitHub Copilot | `~/.copilot/skills/` | `.github/skills/` |
| Windsurf | — | `.windsurf/skills/` |
| Any spec-compliant agent | — | `.agents/skills/` |

Folder names change between tool versions — if a tool doesn't pick it up, check its current skills documentation. Tools without skills support can still use it: paste `SKILL.md` into the tool's rules/instructions file (e.g. `AGENTS.md`, Cursor rules).

## More skills
Full catalogue: [github.com/theaskwhy/skills](https://github.com/theaskwhy/skills)

## Licence
MIT © The Ask Why Company LLC. If you use or adapt this skill, a credit to The Ask Why Company is appreciated.
