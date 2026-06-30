# Tony skills

Each folder here is one **skill**: a `SKILL.md` file describing a capability and
when to use it. At startup Tony scans `skills/*/SKILL.md`, and when something you
say matches a skill's triggers, that skill's instructions are loaded into Tony's
context for that reply — and nothing else is. Small context, focused behaviour.

## Format

```markdown
---
name: Cover Letter
triggers: cover letter, covering letter, application letter
---

# Cover Letter skill

Instructions for Tony go here in plain markdown…
```

- `name` — what the skill is called.
- `triggers` — comma-separated phrases; if any appear in your message, the skill loads.
- Everything after the frontmatter is the instruction body Tony follows.

## Adding a skill

Make a new folder with a `SKILL.md` inside, then restart Tony. That's it —
no code changes. List what's loaded any time at `GET /skills`.
