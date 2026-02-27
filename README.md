# zod4-guide

Zod 4 API guide for AI coding agents. Covers 30+ breaking changes from Zod 3, 9 new APIs, and 7 common pitfalls.

## Why?

AI agents' training data primarily contains Zod 3 syntax. When writing Zod schemas, they often generate deprecated patterns like `z.string().email()`, `{ message: "..." }`, or `z.record(valueSchema)` — all of which are wrong in Zod 4.

This skill ensures agents always use the correct Zod 4 syntax.

## Install

```bash
# Recommended: via skills CLI (auto-tracked on skills.sh)
npx skills add netfishx/zod4-guide

# Or: clone directly into Claude Code skills directory
git clone https://github.com/netfishx/zod4-guide.git ~/.claude/skills/zod4-guide
```

## What's Covered

- **Breaking Changes**: Error customization, string formats, record/enum/object APIs, function/promise schemas, default behavior, type internals
- **New APIs**: Recursive types, template literals, file validation, number formats, string booleans, metadata, JSON Schema, Zod Mini
- **Common Pitfalls**: `$ZodIssue.received` removal, UUID strictness, enum record exhaustiveness, default+optional interaction, error map precedence

## Compatibility

- Zod `^4.0.0`
- Works with: Claude Code, Cursor, Windsurf, and any agent supporting [agent skills](https://vercel.com/kb/guide/agent-skills-creating-installing-and-sharing-reusable-agent-context)

## License

MIT
