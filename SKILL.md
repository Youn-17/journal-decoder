---
name: journal-compass
description: |
  Distill a journal into a reusable submission companion.
  把一本期刊蒸馏成一个可复用的投稿伴侣技能。
  Learns the journal's topic taste, writing style, author guidelines, and aims & scope —
  reading open-access full texts where available — then guides four steps:
  TOPIC (fit verdict) → WRITE (section framework) → POLISH (house style) → SUBMIT (cover letter, title page, declarations).
  它读懂这本刊的选题方向、写作风格、作者指南与 aims & scope（有开放获取全文时连正文一起读），
  带你走完四步：选题适配判断 → 章节框架写作 → 按刊风格润色 → 生成投稿材料（cover letter、title page、声明清单）。
  Two ways in: (1) a journal name → distill directly; (2) a vague need → recommend candidates first.
  Triggers: "distill journal X", "蒸馏 X 期刊", "这篇适合投 X 吗", "按 X 风格写/改",
  "帮我写投 X 的 cover letter / title page", "我这个研究投哪本刊好", "更新 X 期刊的 skill".
---

# Journal Compass

A skill that studies one journal and builds a standalone `<journal-slug>-fit` companion for it.

---

## What the companion covers

| Step | What it does |
|------|-------------|
| **1 · TOPIC** | SUBMIT / RESHAPE / REDIRECT verdict, with topic angles that fit the journal |
| **2 · WRITE** | Section-by-section framework drawn from the journal's own papers |
| **3 · POLISH** | Before → after edits toward the journal's style; clears desk-reject red flags |
| **4 · SUBMIT** | Cover letter, title page checklist, highlights, declarations checklist |

No paid APIs required — runs on standard web access and PDF reading.

---

## How it works

**Read three things about the journal, then compare them:**

| What | Where | What it tells you |
|------|-------|-------------------|
| What it **claims** to want | Aims & Scope, guidelines | The official position |
| What it **actually publishes** | Recent papers + open-access full texts | The real picture |
| What it **rejects** | Reviewer guidelines, desk-reject signals, community reports | The hidden filter |

The most useful finding is usually the gap between what a journal claims and what it actually publishes — e.g. a journal says it welcomes theory but publishes under 2% theory papers means theory-only submissions are at high risk. Always compare the two.

**Three stages every paper must clear:**

Editor's desk → peer review → the shape of accepted papers. The companion maps your work to each stage so you know *where* a paper would fail, not just whether it fits.

**The rival-journal test:**

A finding goes into the profile only if it would change which of two similar journals you'd submit to. Anything both journals want equally is a field-wide norm, not this journal's specific preference — discard it. This is why you always compare against one rival journal.

---

## Build workflow

Seven steps. Pause at the two ⏸ checkpoints for the author's sign-off.

### Step 1 — Set up

Confirm the exact journal (full name + publisher; distinguish look-alikes), pick one rival journal for comparison, ask what material the author has on hand, and decide depth (quick = editor screen only; full = all four steps, default). Check `.claude/skills/*-fit/` — if a skill exists, switch to "Updating."

Create the self-contained folder before starting research:

```
.claude/skills/<journal-slug>-fit/
├── SKILL.md
└── references/
    ├── evidence/
    │   ├── claims.md             # what it says it wants
    │   ├── published.md          # what it actually publishes (≥5 papers)
    │   ├── rejected.md           # what gets rejected and why
    │   ├── guidelines.md         # cover letter, title page, declarations
    │   ├── writing-framework.md  # section moves from open-access full texts
    │   └── rival-<slug>.md       # how it differs from the rival
    └── corpus/                   # PDFs, guideline snapshots
```

### Step 2 — Gather evidence

Fill each file. Parallelize with subagents if available. Every claim needs a source URL and a confidence tag (first-hand > second-hand > inferred).

- **claims.md** — Aims & Scope, editorials
- **published.md** — ≥5 recent papers: topic patterns, contribution-type mix, hot/saturated/gap areas
- **rejected.md** — reviewer guidelines, desk-reject signals, author-forum reports
- **guidelines.md** — Guide for Authors: word/abstract limits, highlights, what a cover letter should contain, what goes on the title page (and what to strip for anonymized review), mandatory declarations
- **writing-framework.md** — find 2–3 open-access full texts; extract the move structure per section (the rhetorical sequence, not the content). If no OA full text is available, say so and note the framework is inferred
- **rival-\<slug\>.md** — for 2–3 topics: how would this journal handle it vs the rival? Tag identical items as `field-wide`

> ⏸ **Checkpoint 1** — Show a summary: source counts, top topics, sharpest claims-vs-reality gaps, whether OA full text was found, key submission-kit items, rival contrast.

### Step 3 — Name the gaps

List every place the journal's claims diverge from what it publishes. Each gap becomes a desk-reject risk or a usable insight. Keep this list — it drives the most useful parts of the verdict later.

### Step 4 — Build the profile

Read `references/signal-mining.md`, then write the profile organized by three stages. Apply the rival-journal test to every finding; drop `field-wide` ones. Aim for 3–7 Stage-1 findings.

> ⏸ **Checkpoint 2** — Show Stage-1 findings with evidence, the "this vs rival" one-liner, the gaps, the writing framework skeleton, and the submission checklist.

### Step 5 — Calibrate

- **Hit test**: 2 in-journal papers held out from Step 2 → must score SUBMIT
- **Redirect test**: 1 rival-journal or off-topic paper → must score REDIRECT with a correct reason

Both must pass before proceeding. Use a subagent to avoid grading your own work.

### Step 6 — Write the child skill

Read `references/fit-skill-template.md` and fill it. The skill must cover all four steps (verdict + angles, writing framework, polish edits, submission kit). Write to `<journal-slug>-fit/SKILL.md`.

### Step 7 (optional) — Check triggers

Do the description triggers match how users actually ask? Is each step's instruction specific enough to act on?

---

## Entry points

**Named journal** → Step 1.

**Vague need** ("Where should I submit a study on GenAI and learning analytics?") → recommend 2–3 contrasting candidates first:

```
### Candidate: [Full name]   ⚡ ready to use / 🆕 needs distilling
Position: [one line — what it publishes and for whom]
Why it fits: [match to topic, method, stage]
Risk: [acceptance bar, likely sticking points]
vs the others: [the key trade-off]
```

Check `.claude/skills/*-fit/` first — an already-distilled journal is ready immediately.

---

## Child skill requirements

The `<journal-slug>-fit` skill must:

1. Take an idea or abstract → return SUBMIT / RESHAPE / REDIRECT with per-stage reasoning
2. Identify which stage fails and what specific change fixes it
3. Provide a fill-in abstract template and title patterns, each anchored to a real published example
4. Generate a cover letter draft, a title-page checklist, and a declarations checklist
5. State limits honestly: sample size, research date, and that fit improves odds but does not guarantee acceptance

---

## Updating an existing skill

1. Read the existing SKILL.md, find the research date, note how stale it is
2. Re-collect only what changes: latest papers, guideline updates, editorial-board changes
3. Reconcile findings: reinforce, update, or add as appropriate
4. Update the "recent shifts" note and research date — incremental, not a full rewrite

---

## Honesty

- Never invent acceptance rates, review timelines, or preferences not supported by evidence
- Never present a field-wide norm as this journal's specific taste
- Always surface the gap between what a journal claims and what it publishes
- The submission kit is a draft — authors should verify against the live Guide for Authors before submitting
- Fit improves the odds; it is not a guarantee

---

## Credits

Footer for child skills:
`> Generated by Journal Compass · researched [date] · [N] papers · https://github.com/Youn-17/journal-compass`
