# ✨ Tony skills

<style>
  @keyframes fadeInDown {
    from {
      opacity: 0;
      transform: translateY(-20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  @keyframes pulse {
    0%, 100% {
      opacity: 1;
    }
    50% {
      opacity: 0.7;
    }
  }

  @keyframes slideInRight {
    from {
      opacity: 0;
      transform: translateX(-20px);
    }
    to {
      opacity: 1;
      transform: translateX(0);
    }
  }

  @keyframes gradient {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }

  h1 {
    animation: fadeInDown 0.6s ease-out;
  }

  h2 {
    animation: slideInRight 0.8s ease-out;
    color: #0366d6;
  }

  code {
    background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
    color: white;
    padding: 2px 6px;
    border-radius: 3px;
  }

  li {
    animation: slideInRight 1s ease-out backwards;
  }

  li:nth-child(1) { animation-delay: 0.1s; }
  li:nth-child(2) { animation-delay: 0.2s; }
  li:nth-child(3) { animation-delay: 0.3s; }
  li:nth-child(4) { animation-delay: 0.4s; }
</style>

Each folder here is one **skill**: a `SKILL.md` file describing a capability and
when to use it. At startup Tony scans `skills/*/SKILL.md`, and when something you
say matches a skill's triggers, that skill's instructions are loaded into Tony's
context for that reply — and nothing else is. Small context, focused behaviour.

## 🎯 Format

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

## 🚀 Adding a skill

Make a new folder with a `SKILL.md` inside, then restart Tony. That's it —
no code changes. List what's loaded any time at `GET /skills`.

---

### 📊 Language Composition

- **Python** - 50.3% 🐍
- **HTML** - 49.7% 🌐
