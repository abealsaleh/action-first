# action-first

A Claude Code **output style** plugin that makes responses action-first:
lead with the next action, number multi-step work, suppress tangents, restate
state every turn, give concrete time estimates, make wins visible.

The ruleset ships as a native output style, baked into the system prompt for
the whole session — no per-invocation command needed.

## Install

```bash
claude plugin marketplace add ~/repos/action-first
claude plugin install action-first@action-first
```

## Activate

`/config` → **Output style** → select **Action First**. Takes effect on the next
session or after `/clear`. The choice persists across sessions (stored in the
`outputStyle` settings key).

## Deactivate

`/config` → **Output style** → select the default style.

## Update

Edit `output-styles/action-first.md`, then run
`claude plugin marketplace update action-first` and start a new session.

## License

MIT. Adapted from [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd) (MIT).
