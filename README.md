# practical-ai-tip

An agent skill that shares practical tips for working with AI assistants and agents. It runs in Claude Code and Claude Cowork.

Call the skill, with or without a question. It reads the current conversation, matches the situation against a curated bank of tips, and shares the best one to three. When only one tip fits, it shows the full tip: what to do, when to use it, the steps, any prompt or template to copy, and its limits. Each tip credits the people and documents it comes from.

## What it helps with

- The AI repeats a mistake, or answers get worse in a long session
- Too many permission prompts
- An agent drifts from the task or stops early
- How to brief an agent, check its work, automate a task, or connect tools safely
- Which practice fits the work at hand

It does not cover AI news, model comparisons or building AI products.

## Install

### Claude Code: plugin (gets updates)

In a Claude Code session:

```
/plugin marketplace add gloriamu0001/practical-ai-tip
/plugin install practical-ai-tip@practical-ai-tip
```

Without a GitHub SSH key, set `CLAUDE_CODE_PLUGIN_PREFER_HTTPS=1` in the shell before starting Claude Code.

To receive new tips automatically, open `/plugin`, go to **Marketplaces**, select `practical-ai-tip` and select **Enable auto-update**. Otherwise run `/plugin marketplace update practical-ai-tip` from time to time.

### Claude Code: copy the folder

Copy `plugins/practical-ai-tip/skills/practical-ai-tip/` into `~/.claude/skills/`. Copy it again to get new tips.

### Claude Cowork

Download [practical-ai-tip.zip](https://github.com/gloriamu0001/practical-ai-tip/releases/latest/download/practical-ai-tip.zip) and upload it in the Claude app's skill settings. Download and upload again to get new tips.

## Use

- **Plugin install:** `/practical-ai-tip:practical-ai-tip`
- **Copied folder:** `/practical-ai-tip`

Add a struggle, the kind of tip wanted, a tip number, or `all` to browse every tip by topic. Asking for a tip on working better with AI also starts the skill.

## About the tips

The maintainer selects, writes and updates the tips. This repository holds only the finished skill; it does not accept contributions to the tip bank.

## License

[CC BY 4.0](LICENSE). Prompts and templates quoted inside tips remain the work of their authors, who are credited in each tip's sources.
