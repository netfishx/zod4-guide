# zod4-guide

A [Claude Code skill](https://docs.anthropic.com/en/docs/claude-code/skills) that teaches Claude the correct Zod 4 APIs, preventing it from falling back to outdated Zod 3 patterns.

## Why?

Claude's training data primarily contains Zod 3 syntax. When writing Zod schemas, it often generates deprecated patterns like `z.string().email()`, `{ message: "..." }`, or `z.record(valueSchema)` — all of which are wrong in Zod 4.

This skill provides a quick-reference of **30+ breaking changes**, **9 new APIs**, and **7 common pitfalls** so Claude always uses the correct Zod 4 syntax.

## Install

```bash
# Clone into your Claude Code skills directory
git clone https://github.com/<your-username>/zod4-guide.git ~/.claude/skills/zod4-guide
```

Or copy `SKILL.md` manually into `~/.claude/skills/zod4-guide/SKILL.md`.

## What's Covered

- **Breaking Changes**: Error customization, string formats, record/enum/object APIs, function/promise schemas, default behavior, type internals
- **New APIs**: Recursive types, template literals, file validation, number formats, string booleans, metadata, JSON Schema, Zod Mini
- **Common Pitfalls**: `$ZodIssue.received` removal, UUID strictness, enum record exhaustiveness, default+optional interaction, error map precedence

## Compatibility

- Zod `^4.0.0`
- Claude Code (any version with skills support)

## License

MIT
