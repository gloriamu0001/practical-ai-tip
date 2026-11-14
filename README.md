# practical-ai-tip

An agent skill that shares practical tips for working with AI assistants and agents. It runs in Claude Code, Codex, Gemini CLI, GitHub Copilot, Cursor and Windsurf.

Call the skill, with or without a question. It reads the current conversation, matches the situation against a curated bank of 89 tips, and shares the best one to three. When only one tip fits, it shows the full tip: what to do, when to use it, the steps, any prompt or template to copy, and its limits. Each tip credits the people and documents it comes from.

## What it helps with

- The AI repeats a mistake, or answers get worse in a long session
- Too many permission prompts
- An agent drifts from the task or stops early
- How to brief an agent, check its work, automate a task, or connect tools safely
- Which practice fits the work at hand

It does not cover AI news, model comparisons or building AI products. Some tips use features of Claude Code; the skill shares those only in Claude Code.

## How the tips are made

Every tip is hand-curated and checked against a written standard.

- **Qualified sources only.** Tips come from the makers of AI tools, the people who build them, recognised practitioners and expert bodies. Anonymous posts, engagement bait and AI-written summaries are rejected.
- **Six quality bars.** A tip must come from a reputable source, be confirmed by at least one other author, apply beyond a single field, be about working with AI, give steps a newcomer can follow, and hold for current tools. A tip that fails one bar is dropped.
- **Disagreements shown, not hidden.** Newer advice replaces older advice from the same source, and official documentation decides questions about a tool's own features. When reputable sources disagree on practice, the tip follows the mainstream practice and marks the other view in a "Sources disagree" note that links to both.
- **One clear format.** One idea per tip, plain language, a source for every factual claim, no hype, and short limits that say where the tip stops working.
- **Tested.** 33 test conversations check that the skill picks the right tip, and that it shares nothing when no tip fits. In the latest run, the first tip shared was correct in 96% of cases, and every no-tip case got no tip.
- **Kept current.** The sources are reviewed every month. Each change is reviewed by the maintainer before it is released.
- **Light at run time.** The skill reads only its own files. It writes nothing, fetches nothing from the network, and keeps no record of the tips it has shown.

## Install

### Any of the six tools, with one command

```
npx skills add gloriamu0001/practical-ai-tip -g
```

Choose the tools when asked, or name them: `-a claude-code codex gemini-cli github-copilot cursor windsurf`. Run `npx skills update` to get new tips.

### Claude Code as a plugin (gets updates)

In a Claude Code session:

```
/plugin marketplace add gloriamu0001/practical-ai-tip
/plugin install practical-ai-tip@practical-ai-tip
```

Without a GitHub SSH key, set `CLAUDE_CODE_PLUGIN_PREFER_HTTPS=1` in the shell before starting Claude Code. To receive new tips automatically, open `/plugin`, go to **Marketplaces**, select `practical-ai-tip` and select **Enable auto-update**.

### By hand

Copy the folder `skills/practical-ai-tip/` into the skills folder of the tool:

| Tool | Folder |
|---|---|
| Claude Code | `~/.claude/skills/` |
| Codex, Gemini CLI, GitHub Copilot, Cursor, Windsurf | `~/.agents/skills/` |

Copy it again to get new tips.

## Use

| Tool | Call the skill |
|---|---|
| Claude Code | `/practical-ai-tip` (as a plugin: `/practical-ai-tip:practical-ai-tip`) |
| Codex | `$practical-ai-tip` |
| Cursor, Windsurf | `/practical-ai-tip` |
| Gemini CLI, GitHub Copilot | ask for a tip; the tool starts the skill |

Add a struggle, the kind of tip wanted, a tip number, or `all` to browse every tip by topic. In every tool, asking for a tip on working better with AI also starts the skill.

## About the tips

The maintainer selects, writes and updates the tips.

## License

[CC BY 4.0](LICENSE). Prompts and templates quoted inside tips remain the work of their authors, who are credited in each tip's sources.
