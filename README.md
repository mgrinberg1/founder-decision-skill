# Founder Decision Copilot 🧭

A [Claude](https://claude.com/claude-code) **skill** that acts as a sharp, experienced
co-founder for the hard calls — pricing, hiring, firing, pivoting, taking investment,
launching, killing a feature, quitting the day job, splitting equity.

It doesn't hand you a balanced pros-and-cons list. It **stress-tests your thinking** like
a demanding partner who's on your side: frames the decision, pokes your weakest
assumption, runs a pre-mortem, checks the call against how startups actually die, applies
distilled lessons from the entrepreneurial canon, and closes with a real recommendation —
plus what would change it.

> The failure mode of "startup wisdom" tools is regurgitating quotes. Nobody's life
> improves because you told them "aim for monopoly." The books are the fuel; the product
> is a **decision process** applied to *your* situation. That's what this is.

## What's inside

```
founder-decision/
├── SKILL.md                         # the 6-step process + the "co-founder who argues" posture
└── references/
    ├── mental-models.md             # 12 models, each with the question it forces on you
    ├── failure-patterns.md          # how startups actually die + recurring anti-patterns
    ├── book-principles.md           # 9 books distilled into applicable principles
    ├── decision-frameworks.md       # pre-mortem, WRAP, two-way doors, expected value…
    └── your-context.example.md      # optional: anchor the copilot to YOUR venture
```

The canon it draws on: *Zero to One*, *The Hard Thing About Hard Things*, *The Lean
Startup*, *Shoe Dog*, *Start-up Nation*, Paul Graham / Y Combinator, Naval, *The
Innovator's Dilemma*, *Crossing the Chasm*.

## How the copilot thinks

Every decision runs through the same process (depth scaled to the stakes):

1. **Is this even the real decision?** — often "should I lower my price?" is really "why
   isn't anyone buying?" It reframes before analyzing.
2. **What kind of door is this?** — reversible (decide fast) vs. irreversible (slow down).
3. **The 2–3 mental models that actually apply** — not a dump; the ones that cut.
4. **A pre-mortem** — "it's a year later and this blew up. Why?"
5. **A check against how startups actually die** — does this push toward or away from a
   known grave?
6. **The canon, applied with judgment** — the idea, not the quote.
7. **The call** — a real lean, its confidence level, and what would change the answer.

## Install

This is a Claude skill. Drop the `founder-decision/` folder into your Claude skills
directory:

**Claude Code (personal skills):**
```bash
cp -R founder-decision ~/.claude/skills/
```

**Project-scoped (share it with a repo's collaborators):**
```bash
cp -R founder-decision /path/to/your/project/.claude/skills/
```

Restart Claude Code (or start a new session) and it'll appear in your available skills.
Then just describe a decision you're weighing — you don't have to name the skill. Things
like *"I'm torn between…"*, *"should I…"*, *"help me decide whether to…"* will trigger it.

## Make it yours (optional)

The skill is generic on purpose — it works for any venture. To anchor it to *your*
business so the advice lands on your reality:

```bash
cd ~/.claude/skills/founder-decision/references
cp your-context.example.md your-context.md
# fill in your market, stage, model, constraints…
```

The copilot reads `your-context.md` automatically if it's there. It's git-ignored in this
repo so your private context never gets committed or shared.

## Extend it

The skill is built to grow. Each reference file is a self-contained, modular knowledge
base — adding to it improves every future decision without touching the core process:

- **A book that shaped you?** Add a section to `references/book-principles.md` — source,
  then a few *applicable* principles (the idea, not a summary), and an "Apply to:" line.
- **A mental model you lean on?** Add it to `references/mental-models.md` in the same
  format: what it is, the question it forces, the failure it prevents.
- **A failure you've lived or witnessed?** Add the pattern to `references/failure-patterns.md`.
- **A decision procedure?** Add it to `references/decision-frameworks.md`.

Keep entries short and *actionable* — the whole design principle is "fuel for a process,"
not a library. Pull requests welcome.

## License

MIT — see [LICENSE](LICENSE). Share it with your founder friends.
