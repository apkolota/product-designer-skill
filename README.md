# Product Designer — a Claude skill

A skill that makes Claude work like an evidence-driven **Senior Product Designer**. It's distilled from years of hands-on practice in B2B SaaS, AI-powered products, agency work and UX research.

It doesn't give Claude a generic "UX checklist". It gives it a way of thinking:

- **No signal, no decision.** Product decisions rest on product signals — or, for new products, on explicit research and written-down assumptions you can come back to.
- **Fix the first experience before adding features.**
- **Hypotheses, triangulation and honest baselines** — shipped vs. baselines set vs. decisions influenced.
- **Prioritise by ownership** — what design can ship at the interface layer now.
- **Precedent first** — how do comparable products solve the same trade-off?
- **Skip research where it's safe** — well-trodden patterns ship on best practice.
- **Minimal, clear UI** that carries the brand's intent.

## What it helps with

| Task | Example prompt |
|---|---|
| Problem framing & hypotheses | "Users generate a draft but don't save it. Frame this." |
| Discovery & research plans | "Plan discovery for a new B2B onboarding flow." |
| Design critique | "Critique this checkout screen" (+ screenshot / Figma link) |
| Prioritisation | "Score these 7 initiatives and tell me what design should own." |
| Usability test plans | "Write a follow-up test comparable to our baseline." |
| Specs & tickets | "Write Jira tickets for a guest-first sign-up flow." |
| Metrics | "How will we know this redesign worked?" |
| AI-feature UX | "Design error recovery for an AI generator." |

## Install

### Claude Code — as a plugin

```
/plugin marketplace add apkolota/product-designer-skill
/plugin install product-designer@product-designer
```

### Claude Code — as a personal skill

```bash
git clone https://github.com/apkolota/product-designer-skill.git
cp -R product-designer-skill/skills/product-designer ~/.claude/skills/
```

Claude loads it automatically for product design tasks, or call it with `/product-designer`.

### Claude.ai

Download `product-designer.zip` from [Releases](../../releases) (or zip the `skills/product-designer` folder) and upload it in **Settings → Capabilities → Skills**.

## Structure

```
skills/product-designer/
├── SKILL.md                    # core beliefs, working loop, answer shape
└── references/
    ├── process.md              # playbooks: research, framing, segmentation, prioritisation, testing, handoff
    ├── critique.md             # critique checklist and output format
    └── templates.md            # bet cards, hypotheses, scoring, tickets, test plans, case studies
```

## License

MIT
