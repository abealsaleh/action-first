# action-first

A Claude Code **output style** plugin that shapes responses for an ADHD reader:
lead with the next action, number multi-step work, suppress tangents, restate
state every turn, give concrete time estimates, make wins visible.

This is a conversion of the [i-have-adhd](https://github.com/ayghri/i-have-adhd)
skill by Ayoub Ghriss into a native Claude Code output style. Instead of a
per-invocation skill plus a SessionStart-hook "always-on" hack, the ruleset is
an output style baked into the system prompt for the whole session.

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

MIT. Derived from [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd) (MIT).
