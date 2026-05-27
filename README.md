# RunDrill Python

Your personal **Python coach** inside your AI agent — for the age when the AI writes the first draft.
Instead of watching code get generated, you **read it, trace it, predict what it does, and review it
for bugs** — including code an AI wrote. Short targeted drills, an honest picture of your level
(novice → expert), and mistake memory that resurfaces what you got wrong. The skill is the voice;
your level, weak topics, and track live on the RunDrill MCP server (`mcp.rundrill.com`), synced
across machines — not in a local file.

**Why this course is different.** When an AI can write any function on demand, the real risk is the
*illusion of competence* — feeling fluent in code you never actually read. RunDrill Python trains the
skills that now matter most: reading, tracing, and **reviewing** code. Its signature drill hands you
plausible AI-written code with a real bug and asks you to find it — like a pull request.

## One plugin, three hosts

The coaching skill (`skills/python-coach/SKILL.md`) and `.mcp.json` are shared; each host reads its
own manifest and ignores the rest.

| Host | Reads |
|---|---|
| Claude Code / Claude Desktop | `.claude-plugin/plugin.json` + `.mcp.json` |
| OpenAI Codex | `.codex-plugin/plugin.json` + `.mcp.json` |
| Google Antigravity | `plugin.json` + `mcp_config.json` (+ `rules/`) |

The MCP endpoint is `https://mcp.rundrill.com/prog` — the programming-course host that Python (and
later Rust, JavaScript) share, passing `language: "python"`. On first use the host opens a browser
tab for the OAuth handshake, then closes it — no API key to paste.

## Install

- **Claude Code / Desktop** — via the RunDrill marketplace:
  ```
  /plugin marketplace add rundrill/marketplace
  /plugin install rundrill-python@rundrill
  ```
  Then run `/python-coach`.
- **OpenAI Codex** — add the RunDrill catalog, then install `rundrill-python`:
  ```
  codex plugin marketplace add rundrill/marketplace
  ```
- **Google Antigravity** — drop this folder into `~/.gemini/config/plugins/rundrill-python/` (global)
  or `<workspace>/.agents/plugins/rundrill-python/` (workspace-scoped).

## License & attribution

© RunDrill. Licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0
International (CC BY-NC-ND 4.0)** — full text in [LICENSE](LICENSE).

In short, you **may** view, run, and share this plugin unchanged, for non-commercial purposes, **as
long as you give credit**. You **may not** use it (or any part, including the coaching skill)
commercially, or publish modified/derivative versions.

Required attribution when sharing: *"RunDrill Python coach — © RunDrill, CC BY-NC-ND 4.0,
https://rundrill.com".*

For commercial use, derivatives, or any other license, contact **hello@rundrill.com**.
