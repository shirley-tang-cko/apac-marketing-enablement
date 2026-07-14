# APAC Marketing Enablement

> The parent repository for all **Checkout.com APAC Marketing** initiatives.
> Houses AI-powered Claude Code skills that standardize and speed up how the regional marketing team plans, briefs, and executes commercial programs.

---

## 📁 Repository Structure

```
apac-marketing-enablement/
└── .claude/
    └── skills/
        └── event-briefing/
            ├── SKILL.md                  # Skill logic & briefing structure
            └── references/
                └── template.html         # CKO-branded briefing template
```

New skills are added under `.claude/skills/<skill-name>/`.

---

## 🧠 Skills

### `event-briefing` — Event Briefing Doc Preparation

Generates a standardized, **CKO-branded event briefing** as a Google Doc in Drive that regional marketers fill in — so the commercial team can foresee and prepare for upcoming events (executive luncheons, roundtables, hosted merchant events).

**Structure** (mirrors the team's house format):

| # | Section | What it captures |
|---|---------|------------------|
| 1 | **Why are we doing this?** | Strategic rationale + competitor benchmarking (what rivals ran, which tier-1 brands they secured) |
| 2 | **Event Overview** | Date, time, expected pax, theme + a Tactical Specifications table (Target Market · Industry Focus · Target Personas · Commercial Pitch) |
| 3 | **Target Account List** | Link to the marketer's separate Google Sheet |
| 4 | **Planning Timeline** | `Party \| Phase \| Duration \| Task`, working back from the event date |
| 5 | **Budget** *(optional)* | Agency quote line items + named Event Agency |

**Two modes:**
- **Blank template** (default) — a fill-in-ready master doc for marketers to complete.
- **Populated briefing** — paste real event details and the skill fills the template, flagging anything outstanding as `[TO CONFIRM]`.

**Output:** a branded Google Doc saved to Drive, with the link shared back.

**Triggers:** `/event-briefing`, "create an event briefing", "event briefing template", "brief the team on an upcoming event".

---

## 🚀 How to Use

These are **Claude Code skills**. To use them:

1. **Clone the repo** (or open it in Claude Code on the web):
   ```bash
   git clone https://github.com/shirley-tang-cko/apac-marketing-enablement.git
   ```
2. Claude Code automatically discovers skills in `.claude/skills/`.
3. Invoke a skill by typing its trigger — e.g. `/event-briefing` — or just describe what you need ("help me brief the team on our Q3 HK luncheon") and Claude activates the right skill.

> **Prerequisite:** the `event-briefing` skill saves to Google Drive, so the **Google Drive connector** must be authorized in your Claude Code session.

---

## 👥 For the Team

- **Adding a new skill:** create `.claude/skills/<name>/SKILL.md` with YAML frontmatter (`name`, `description`, `user-invocable: true`) and any supporting files under a `references/` subfolder.
- **Editing a skill:** update `SKILL.md` (behavior/logic) or `references/` (templates/assets) and commit. Changes are picked up on the next session.
- Keep this repo **APAC-marketing-scoped** — commercial-wide skills live in the main enablement repo.

---

## 🔒 Privacy

This repository contains internal Checkout.com marketing processes and workflow automation. Keep it within the APAC marketing team.

---

## 👤 Maintainer

**Shirley Tang** — APAC Marketing, Checkout.com
