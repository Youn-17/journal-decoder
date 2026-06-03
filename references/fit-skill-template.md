# Child-skill template

Step 6 fills this in to produce `<journal-slug>-fit/SKILL.md`.

**The rule that governs every placeholder**: anchor it to real evidence. If a field says [real example], paste an actual title, abstract sentence, or guideline line from the journal's own papers or documents. Generic advice is the failure mode this template exists to prevent — if you cannot fill a field with real evidence, mark it [NOT SAMPLED] rather than inventing it.

---

```markdown
---
name: [journal-slug]-fit
description: |
  Submission companion for [Journal full name] ([Publisher], ISSN [XXXX-XXXX]),
  distilled from [N] papers + official guidance (researched [YYYY-MM-DD]); rival: [Rival journal].
  Four steps: TOPIC (SUBMIT / RESHAPE / REDIRECT) → WRITE (section framework) → POLISH (house style) → SUBMIT (cover letter, title page, declarations).
  [期刊全名] 的投稿伴侣，基于 [N] 篇论文 + 官方指南（调研日期 [YYYY-MM-DD]）。
  四步：选题适配判断 → 章节框架写作 → 按刊风格润色 → 投稿材料生成（cover letter / title page / 声明清单）。
  Triggers: "is this a fit for [Journal]?", "投 [Journal] 行不行", "这篇适合投 [Journal] 吗",
  "按 [Journal] 风格写/改", "帮我写投 [Journal] 的 cover letter / title page", "[Journal] desk reject risk",
  or pasting an abstract / draft aimed at [Journal].
---

# [Journal full name] — Submission Companion

<!--
HOW TO FILL THIS IN:
Replace every [...] with real content drawn from the evidence files.
The header line below should be one sentence that captures why this journal
exists — what problem it serves, what community it speaks to.
Example: "C&E publishes evidence that a technology changed learning or teaching
in a way that matters beyond one classroom."
Do NOT use marketing language from the Aims & Scope verbatim; write what
the corpus actually shows.
-->

> [One sentence: what this journal actually publishes and who reads it, based on the corpus — not copied from the Aims & Scope.]

First activation only: "Built from [N] published papers + public guidance up to [date]. Reflects what the journal publishes, not the editor's private bar. Fit improves odds — it does not guarantee acceptance. Verify against the live Guide for Authors before submitting."

---

## How this journal selects

<!--
Fill Stage 1 and 2 from the profile built in Step 4.
Stage 3 is covered in the WRITE section below.

For Stage 1 red flags: write them as testable conditions, not abstract principles.
BAD:  "The paper must have broad relevance."
GOOD: "The study is conducted in a single institution with no argument for
       generalizability — desk-reject risk."

Aim for 3–5 red flags, each with a source tag.
-->

**Stage 1 — Editor's desk** (~30 seconds before peer review):
- Scope: [What's in. What's explicitly out. Be specific.]
- Accepted contribution types: [empirical / theory / methods / review / design, and the approximate mix]
- Desk-reject red flags — any one of these blocks the submission:
  1. [Specific condition → source: rejected.md or gap classification]
  2. [...]
  3. [...]
  [Add more if well-supported by evidence]

**Stage 2 — Peer review**:
- Method/rigor bar: [The unstated floor accepted papers share — name it from the corpus, e.g. "studies consistently report effect sizes and confidence intervals; significance alone is not sufficient"]
- Framing requirement: [How a contribution must be argued to satisfy this community — e.g. "the technology must be connected to a named learning construct; describing system features alone is not a contribution"]
- Novelty standard: [What counts as new here — incremental extension OK? replication valued? bold theoretical claim expected?]

---

## STEP 1 · TOPIC

<!--
This section drives the fit verdict. Fill the three sub-sections below from the profile.
The gap list and saturation list should be 3–5 items each, specific enough to act on.
-->

**Verdict logic**: walk Stage 1 and Stage 2; score each PASS / WEAK / FAIL with one line of evidence. Any Stage-1 red flag is an automatic block regardless of Stage 2.

Return one of:
- **SUBMIT** — clears both stages; proceed to WRITE
- **RESHAPE** — right journal, wrong framing; see Reframe playbook below
- **REDIRECT** — won't fit even reshaped; see "Where else it might fit"

**Gaps this journal wants filled** (good angles right now):
- [Specific gap from published.md, e.g. "Longitudinal designs on GenAI use — almost no published examples despite editorial interest"]
- [...]
- [...]

**Saturated zones** (avoid or differentiate strongly):
- [Specific saturated area, e.g. "Single-session ChatGPT accuracy experiments with student satisfaction outcomes"]
- [...]

**Angle finder**: for a rough idea, propose 2–3 framings that land in the gap list above and avoid the saturation list.

**Reframe playbook** (for RESHAPE verdicts):

<!--
Write one reframe move per common failure mode. Each move should be specific:
state what the problem is, what to change, and what the result looks like.
-->

| If the problem is... | Change this | To get this |
|----------------------|-------------|-------------|
| [Common Stage-1 failure, e.g. "No learning outcome measured"] | [Specific change, e.g. "Add a pre/post measure of [construct] using a validated instrument"] | [Result, e.g. "Reframed as an intervention study with measured educational impact"] |
| [Common Stage-2 failure, e.g. "Theory mentioned but not used to explain findings"] | [Change] | [Result] |
| [Another common pattern] | [...] | [...] |

---

## STEP 2 · WRITE

<!--
Fill this section from writing-framework.md and published.md.
Every element must be anchored to a real example — a real title, a real abstract excerpt,
a real section structure you observed in the corpus.
If you did not sample full texts, mark each item [INFERRED FROM ABSTRACTS].
-->

### Abstract

<!--
Format: [structured / unstructured], ≤[N] words.
Then give the fill-in template with labeled sentence functions.
Then paste one real example (DOI or full citation at the end).
-->

Format: [structured / unstructured], ≤[N] words.

Fill-in template:
```
S1: [Function — e.g. "Why this problem or context matters"]
S2: [Function — e.g. "The specific gap or unresolved question"]
S3: [Function — e.g. "What this study did: design + participants in one sentence"]
S4: [Function — e.g. "Method in one clause"]
S5: [Function — e.g. "Key finding with direction and magnitude"]
S6: [Function — e.g. "What this means for [practitioners / researchers / the field]"]
```

Real example:
> "[Paste 1–3 sentences from a real abstract that illustrate the pattern. Include the DOI.]"
> — [Author et al., Year] ([DOI])

Highlights (if required): [count] bullets, ≤[N] characters each including spaces.

### Title

Patterns observed in the corpus:

```
Pattern A: [Description, e.g. "[Construct] in [context]: [method signal]"]
Real example: "[Paste a real title]" ([Year])

Pattern B: [Description, e.g. "The effect of [X] on [Y]: [design signal]"]
Real example: "[Paste a real title]" ([Year])
```

### Introduction

Move structure (from corpus analysis):
```
Move 1: [What the intro opens on — the field's importance, a statistic, a problem]
Move 2: [How it narrows — technology focus, gap in prior work, theoretical framing]
Move 3: [Gap statement — signal words used: "however" / "little is known" / "remains unclear"]
Move 4: [Aim statement — exact phrasing pattern used, e.g. "Therefore, this study aimed to..."]
Move 5: [Contribution + roadmap — stated explicitly or implied?]
Research questions: [Appear at end of Introduction / in a dedicated RQ section before Methods / both]
```

### [Theory / Literature review]

```
[Separate section or folded into Introduction?]
[If separate: what does it contain? One subsection per construct? Hypothesis at end of each subsection?]
[Is a named theoretical framework expected? Where does it appear?]
```

### Methods

Standard subsection sequence:
```
[Participants / Context] → [Design] → [Instruments / Materials] → [Procedure] → [Analysis]
```

Expected detail level:
- Participants: [What to report — N, age range, institution type, sampling method]
- Instruments: [One paragraph per measure: name, source, number of items, reliability statistic, one example item]
- Analysis: [Name the software, the specific procedure, any fit indices or effect size statistics expected]

### Results

```
Organization: by [research question / hypothesis / thematic cluster]
Inline statistics: [format used, e.g. "t(df) = X.XX, p = .XXX, d = X.XX"]
Tables: [what they typically show — descriptives + reliability / model parameters / group comparisons]
Figures: [what they typically show — path diagram with coefficients / bar charts / none]
```

### Discussion

Fixed moves (from corpus analysis):
```
Move 1: Restate aim and key findings [~1 paragraph]
Move 2: Interpret each finding against theory + prior work [signal phrases: "In line with..." / "Contrary to..."]
Move 3: Implications for [practitioners / researchers] [required: what should someone DO with this?]
Move 4: Limitations [grouped by type: sample / design / measurement]
Move 5: Future directions [paired with limitations / free-standing]
```

Conclusion: [separate section / merged with Discussion]

### Length and format

```
Body word limit: ≤[N] words (excluding [references / appendices])
Reference density: approximately [N] citations per 1000 words
Reference style: [APA 7th / Vancouver / journal-specific]
Section numbering: [required / not required]
```

---

## STEP 3 · POLISH

<!--
Write specific polish rules for this journal.
Each rule should reference something specific from the profile — a framing requirement,
a style observation, a red flag — not generic writing advice.
-->

For any draft or paragraph provided, do a **before → after** edit:

1. **Framing check**: [Specific framing requirement — e.g. "Does the study connect its findings to a named learning construct? If not, add one sentence that names the construct and frames the result in those terms."]
2. **Red flag sweep**: run the Stage-1 red flags above. For any that fire, fix it before moving to style.
3. **Abstract**: rewrite to the template above if it doesn't follow the sentence-function sequence.
4. **Title**: retitle to one of the patterns above if the current title doesn't match.
5. **Word limit**: if over [N] words, cut [specific section most likely to be over-long, e.g. "implementation detail in Methods"] first.
6. **[Journal-specific style note, e.g. "Move implementation/architecture detail to URLs or supplementary material — this journal does not publish engineering specifications"]**

---

## STEP 4 · SUBMIT

<!--
Fill from guidelines.md.
Every element should be specific to this journal.
If you could not confirm a requirement, mark it [UNCONFIRMED — check live guide].
-->

### Cover letter

<!--
State whether it's mandatory, recommended, or not mentioned.
Then give the skeleton with labeled beats.
-->

Status: [mandatory / recommended / not mentioned in guidelines]

Skeleton:
```
Dear [Editor name if known / "the Editor"],

[Beat 1: Study aim + main finding in 2–3 sentences. No jargon. What did you do and what did you find?]

[Beat 2: Why this fits [journal name]'s scope. Use the journal's own scope language.]

[Beat 3: What is novel and why it matters beyond this study.]

[Beat 4: Originality statement — not published, not under consideration elsewhere. Preprint may be mentioned if applicable.]

[Beat 5 (optional): If invited to submit (special issue, editor invitation), mention it here.]

Sincerely,
[Corresponding author name, affiliation, email]
```

Do NOT include in the cover letter:
- [List specific exclusions found in guidelines — e.g. "funding sources", "suggested reviewers", "author declarations" — these go in the submission system or the manuscript]

### Title page

<!--
If double-blind review: give two lists — what goes on the title page, and what to strip from the manuscript.
If single-blind: give the title-page requirements only.
-->

[If double-blind review:]

Elements for the separate title page:
```
☐ Article title
☐ All author names (exact order matching submission system)
☐ Each author's affiliation (department, institution, city, country)
☐ Corresponding author: full postal address + email
☐ [Any additional fields required by this journal — e.g. ORCID, present address, funding source]
☐ Acknowledgements (title page ONLY — not in the anonymized manuscript)
☐ [Any declarations that go on the title page rather than as separate files]
```

Anonymization strip-list (apply to the manuscript file):
```
☐ Author names and affiliations (remove from body, header, footer)
☐ Acknowledgements (move to title page)
☐ Funding statements (move to title page or restore at acceptance)
☐ Self-citations: "Smith et al. (2022) showed..." → "[Anonymous, 2022] showed..."
☐ Self-citations in reference list: "[Anonymous, 2022] Details omitted for review."
☐ Institutional identifiers in figures or supplementary files
☐ Document metadata: clear the author field in file properties
```

### Declarations checklist

<!--
List every declaration this journal requires.
For mandatory ones, mark them clearly so the author doesn't skip them.
Include the standard template wording where available.
-->

```
☐ [MANDATORY] Declaration of Competing Interest
   Standard: "The authors declare no competing financial interests or personal relationships."
   Or: list each disclosed interest by author.
   Placement: [separate file via declarations tool / end of manuscript before references]

☐ [MANDATORY] CRediT Author Contribution Statement
   Format: "[Author A]: Conceptualization, Methodology, Writing – original draft.
            [Author B]: Formal analysis, Visualization.
            [Author C]: Supervision, Writing – review & editing."
   Placement: [end of manuscript / separate file]

☐ [MANDATORY] Data Availability Statement
   Options: "Data are available at [repository] [DOI]."
   Or: "Data cannot be shared publicly because [reason]."
   Placement: [end of manuscript]

☐ [MANDATORY] Funding Statement
   Standard if funded: "This work was supported by [Funder] [grant number]."
   Standard if not: "This research received no specific grant from any funding agency."
   Placement: [end of manuscript / title page — check guidelines]

☐ [IF HUMAN SUBJECTS] Ethics and Informed Consent
   Standard: "This study was approved by [IRB/Ethics Committee name] (approval no. [XXX]).
              Informed consent was obtained from all participants."
   Placement: [Methods section or end of manuscript]

☐ [IF AI USED IN WRITING] Generative AI Declaration
   Standard: "During preparation of this work, the author(s) used [Tool] to [reason].
              The author(s) reviewed and edited the content and take full responsibility
              for the published article."
   Placement: [before the reference list, in a dedicated section]
   Note: Basic grammar/spell-check tools do not require a declaration.
```

### Format checklist

```
☐ Body word count ≤[N] words (excluding references and appendices)
☐ Abstract ≤[N] words, [structured / unstructured]
☐ Highlights: [3–5] bullets, ≤[N] characters each (including spaces); submitted as separate file
☐ Reference style: [APA 7th / Vancouver / etc.]
☐ File format: [.docx single-column / .tex with journal template / etc.] — PDF source not accepted
☐ Section numbering: [required: 1, 1.1, 1.1.1 / not required]
☐ Figures: [one file per figure / embedded / dpi requirement]
☐ Tables: [editable text, not images]
```

---

## Where else it might fit

Submit to [Journal full name] rather than [Rival] when: [specific distinguishing condition — what this journal accepts that the rival doesn't or vice versa].

If the work leans toward [specific type, e.g. "pure theory, methodological development, or a single-institution report"], [Rival] is a better fit because [specific reason].

Other candidates:
- [Any other relevant journals worth mentioning, with one-line rationale]

---

## Limits

- Reflects published taste up to [YYYY-MM-DD]. Cannot capture editorial decisions made after that date.
- Built from [N] papers and public guidance. Does not reflect internal editorial standards or unpublished preferences.
- [Indicate any gaps — e.g. "Writing framework inferred from abstracts only; no OA full texts were sampled."]
- Fit improves the odds. It is not a guarantee of acceptance.
- The submission kit is a draft. Verify every element against the live Guide for Authors before submitting.
- Sample: [N] papers; rival: [Rival journal].

## Evidence

All evidence files are in `references/evidence/`:
- `claims.md` — what the journal says it wants (aims & scope, guidelines)
- `published.md` — what it actually publishes (corpus analysis)
- `rejected.md` — what it rejects (reviewer criteria, desk-reject signals)
- `guidelines.md` — submission requirements (cover letter, title page, declarations, format)
- `writing-framework.md` — section-by-section move structure [from OA full texts / inferred from abstracts]
- `rival-[slug].md` — comparison against [Rival journal]

---

> Generated by Journal Compass · researched [date] · [N] papers · https://github.com/Youn-17/journal-compass
```
