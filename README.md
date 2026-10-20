# Claude-Code-Feedback

A Claude Code plugin for filing well-formed issues against [anthropics/claude-code](https://github.com/anthropics/claude-code).

Each skill fetches the live GitHub issue template, gathers required fields (version, OS, reproduction steps, model, etc.), builds a preview, and submits via `gh issue create` once confirmed.

## Skills

| Skill | Use for |
|-------|---------|
| `feedback-bug` | CLI bugs — crashes, hook failures, permission prompts, MCP config, settings.json issues |
| `feedback-model-behavior` | What the model produced — wrong answer, bad code, unwanted edits, unwarranted refusal |
| `feedback-feature-request` | Missing functionality |
| `feedback-docs` | Documentation issues — wrong, outdated, or missing docs |
| `feedback-refresh-templates` | Refresh cached Anthropic issue templates when they drift |

## Requirements

- `gh` CLI, authenticated against a GitHub account
- `curl` (for fetching live templates)

## Why separate from meta-tools

Originally bundled in `Claude-Meta-Tools-Plugin`. Split out because issue filing is a focused, self-contained concern and "meta-tools" was too vague for discovery.

## License

MIT
