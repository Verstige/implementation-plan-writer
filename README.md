# Implementation Plan Writer: Bite-Sized Tasks, Paths

> Turn a request into a plan an agent can execute. Bite-sized tasks, real file paths, ordered by dependency, with the verification step written in.

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg) ![Claude Code](https://img.shields.io/badge/Claude_Code-skill-blueviolet.svg) [![Available on Agensi](https://img.shields.io/badge/Agensi-%245-ff5a5f.svg)](https://agensi.io/skills/implementation-plan-writer-bite-sized-tasks-paths)

## What it does

Write implementation plans: bite-sized tasks, paths, code.

Write comprehensive implementation plans assuming the implementer has zero context for the codebase and questionable taste. Document everything they need: which files to touch, complete code, testing commands, docs to check, how to verify. Give them bite-sized tasks. DRY. YAGNI. TDD. Frequent commits.

## The failure it prevents

Working this by hand means rediscovering the same edge cases every time. They are written down here instead, with the fix for each one.

## When to use it

- Implementing multi-step features
- Breaking down complex requirements
- Delegating to subagents via subagent-driven-development
- Feature seems simple (assumptions cause bugs)
- You plan to implement it yourself (future you needs guidance)
- Working alone (documentation matters)

## What's inside

```
plugins/
└── implementation-plan-writer/
    ├── .claude-plugin/plugin.json
    └── skills/implementation-plan-writer/
        ├── SKILL.md
```

## Install

Add this repo as a Claude Code marketplace, then install the skill:

```bash
claude plugin marketplace add Verstige/implementation-plan-writer
claude plugin install implementation-plan-writer@implementation-plan-writer
```

Or copy the skill straight into your skills directory:

```bash
git clone https://github.com/Verstige/implementation-plan-writer.git
cp -R implementation-plan-writer/plugins/implementation-plan-writer/skills/implementation-plan-writer ~/.claude/skills/
```

## Usage

The skill activates on the work it describes. Ask for the outcome, and it
supplies the method:

```
> "turn a request into a plan an agent can execute"
```

## License

MIT. Adapted from [obra/superpowers](https://github.com/obra/superpowers), which is MIT licensed. See [LICENSE](LICENSE) and [NOTICE](NOTICE).

---

**Also available as a paid skill on Agensi** — $5. Install it with one command, no clone required:

[agensi.io/skills/implementation-plan-writer-bite-sized-tasks-paths](https://agensi.io/skills/implementation-plan-writer-bite-sized-tasks-paths)

Part of the [Verstige](https://github.com/Verstige) skills portfolio. More at [github.com/Verstige](https://github.com/Verstige).
