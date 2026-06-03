# Signal Mining

How to turn raw evidence (claims / published / rejected / full texts / guidelines) into a tight, accurate journal profile. Read this during Step 4.

---

## 1. From candidate observation to real finding

Something you noticed in the corpus is only a candidate. Every candidate must pass both tests before entering the profile.

### Test 1 — Rival-journal test

> Would knowing this change which of two similar journals you'd submit to?

Run the test mentally: if both this journal and the rival journal would accept a paper on this point equally, the finding is a field-wide norm — discard it.

**Fail examples** (both journals want this → discard):
- "Papers use IMRaD structure"
- "Papers have a limitations paragraph"
- "Papers cite recent literature"
- "Papers are well-written"
- "Papers state their contribution clearly"

**Pass examples** (this journal specifically wants this, rival does not):
- "Requires a real classroom intervention with students, not a lab simulation" (Computers & Education vs BJET)
- "Expects a named theoretical framework as its own section, not folded into the literature review" (JLS vs AERA Open)
- "Rewards replication and consolidation over novel methods" (Psychological Science vs JPSP)
- "Desk-rejects systematic reviews without a registered protocol" (BMJ vs JAMA)

### Test 2 — Prediction test

> Can this finding predict the fate of a paper you haven't seen?

If you cannot say "a paper with property X would likely be desk-rejected / welcomed here," the finding is not actionable — discard it.

**Fail examples** (cannot predict):
- "This journal values quality research"
- "Papers should be methodologically rigorous"
- "Papers address important questions"

**Pass examples** (predicts a specific outcome):
- "A paper reporting only satisfaction/intention-to-use with no learning outcome measure will be desk-rejected here"
- "A paper that reports a novel AI architecture without measuring educational impact will be routed to the companion journal"
- "A study with N < 50 that does not justify the sample size will likely fail peer review"

### Decision table

| Passes Test 1 | Passes Test 2 | Action |
|:---:|:---:|--------|
| ✓ | ✓ | **Real finding** — add to profile |
| ✓ | ✗ | **Descriptive label** — note in profile text, don't use in verdict logic |
| ✗ | ✓ | **Field-wide norm** — discard; it gives no advantage |
| ✗ | ✗ | **Discard** |

> Aim for 3–7 Stage-1 findings that pass both tests. Three strong ones beat ten weak ones.

---

## 2. Claims-vs-reality gap: how to extract and classify

The gap between what a journal claims and what it publishes is the richest source of non-obvious findings.

### Extraction process

1. List every claim from `claims.md` (stated preferences, scope descriptions, "we welcome X" language)
2. For each claim, check `published.md`: does the corpus actually reflect it?
3. Where they diverge, record the gap with approximate magnitude (e.g. "claims to welcome theory; empirical papers are ~95% of corpus in last 3 years")
4. Classify the gap type:

| Type | Pattern | What to tell the author |
|------|---------|------------------------|
| **Aspirational** | Claims to want X, publishes very little X | Frame X as support for the main empirical contribution, not as the contribution itself. X-only submissions face desk-reject risk. |
| **Narrower than stated** | Broad scope claim, actual publications cluster tightly | The working scope is narrower than advertised. Name the cluster and advise positioning inside it. |
| **Drifting** | Recent 1–2 years diverging from older issues | A transition is underway. Weight recent papers heavily; flag the direction. |
| **Hidden bar** | "Welcomes all methods" but accepted papers share an unstated rigor floor | Name the floor concretely: "accepted papers consistently report [specific statistic / sample threshold / instrument validation]". |

### Gap as a desk-reject signal

Every Aspirational or Hidden-bar gap becomes a Stage-1 red flag in the profile. State it as a testable condition:

```
❌ "The main contribution is a new AI model / algorithm / system, with learning impact as secondary"
   → Stage 1 block: contribution type mismatch. Route to [companion journal].

❌ "The study has no control group or comparison condition"
   → Stage 1 / Stage 2 risk depending on whether guidelines state it or reviewers catch it.
```

### Gap as a hidden preference to exploit

Every Narrower-than-stated gap is an opportunity. If the journal quietly prefers a sub-area it doesn't advertise, say so:

```
✅ Gap insight: Although the journal's Aims & Scope mention "all educational technologies,"
   62% of papers in 2022–2024 involve generative AI or learning analytics.
   → Framing a study within these areas improves fit even if the topic itself is unusual.
```

---

## 3. Writing style: measure, don't describe

Pull 5–10 recent representative papers (full text where available, abstracts only if not). Measure each dimension rather than forming an impression.

### Abstract

| Measure | How |
|---------|-----|
| Structured vs unstructured | Does it have labeled sections (Background, Methods, etc.)? |
| Word count | Count 5 abstracts; record min / median / max |
| Sentence functions | Label each sentence: problem / gap / aim / design / participants / method / finding / implication. Which are always present? Which are optional? |

Record as a fill-in template, not a description:

```
Abstract template (≤[N] words, unstructured):
S1 [Why this problem matters in [field/context]]
S2 [The specific gap or unresolved question]
S3 [What this study did: design + participants]
S4 [Method in one clause]
S5 [Key finding with direction and magnitude]
S6 [What this means for [practitioners / researchers / the field]]
```

Anchor it to one real example:
```
Real example (doi: ...):
"[paste 1–2 sentences that exemplify the pattern]"
```

### Title

Measure across 10 recent titles:
- Average word count
- Use of colon subtitle (X of Y: a Z study) — what % use it?
- Does the title name the construct / population / method / technology?
- Is it a declarative finding or a descriptive topic phrase?

Record as 2–3 named patterns with a real example of each:

```
Pattern A: [Construct] in [context]: [method signal]
  → "Self-regulated learning in online courses: A quasi-experimental study"

Pattern B: The effect of [technology] on [construct]: [method signal]
  → "The effect of GPT scaffolding on academic writing: An experiment with undergraduate students"
```

### Introduction move structure

Read 3 introductions in full and map the moves:

```
Move 1 — Establish importance: [what does it open on? the field? the problem? a statistic?]
Move 2 — Narrow to the specific topic: [how many paragraphs? reference to technology or theory?]
Move 3 — State the gap: [signal words used: "however", "little is known", "remains unclear"?]
Move 4 — State the aim: [exact phrasing pattern: "Therefore, this study..." / "The purpose of this paper is to..."]
Move 5 — Contribution/roadmap: [stated explicitly or implied? RQs here or in their own section?]
```

Note where the research questions appear: end of introduction, or in a dedicated "Research questions" section before Methods.

### Methods

Note the standard subsection order and the expected level of detail for each:

```
Typical structure: Participants → Design → [Intervention / Materials] → Measures → Analysis
Detail expected for Measures: [one paragraph per instrument: name + source + N items + reliability (Cronbach's α or similar) + one example item]
Detail expected for Analysis: [name the software + the specific procedure + any fit indices reported]
```

### Results

Note whether results are organized by research question or by hypothesis, and how statistics are reported:

```
Organization: by [RQ / hypothesis / thematic cluster]
Inline reporting pattern: t(df) = X.XX, p = .XXX, d = X.XX
Table role: [descriptives + reliability / model parameters / group comparisons]
Figure role: [path diagram with coefficients / bar charts with error bars / none typical]
```

### Discussion

Map the fixed moves across 3 discussions:

```
Move 1 — Restate aim and key findings (1 paragraph)
Move 2 — Interpret each finding against theory and prior work ("In line with...", "Contrary to...")
Move 3 — Implications for [practitioners / policymakers / researchers] (required: what should someone DO?)
Move 4 — Limitations (grouped by type: sample, design, measurement)
Move 5 — Future directions (paired with each limitation or free-standing?)
```

Note if Conclusion is a separate section or merged into Discussion.

### Length and format

| Parameter | Record |
|-----------|--------|
| Body word count | min / median / max from 5 papers (exclude refs/appendices) |
| Reference density | citations per 1000 words (approximate) |
| Recency of citations | % of references from last 5 years (approximate) |
| Self-citation to journal | whether papers typically cite the same journal |
| Section numbering | numbered (1, 1.1) or unnumbered? |
| Reference style | APA 7th / Vancouver / Chicago / journal-specific? |

---

## 4. From author guidelines to submission kit

The Guide for Authors is a checklist. Convert it into ready-to-fill templates.

### Cover letter

Find whether the journal expects a cover letter (mandatory, recommended, or not mentioned). Then record:

**What to include** — list only what this journal specifically asks for or Elsevier/Springer/Wiley guidance specifies:
```
[1] Study aim + main finding (2–3 sentences, no jargon)
[2] Why this fits [journal name]'s scope (one sentence, using the journal's own scope language)
[3] What is novel and why it matters beyond this study
[4] Originality statement: not published, not under consideration elsewhere
[5] [Optional] If invited: note the special issue or editor invitation
```

**What NOT to include** (common mistakes that some journals explicitly prohibit):
```
- Funding sources or declarations (go in the manuscript or the submission system)
- Suggested or excluded reviewers (go in the submission system)
- Author biographical notes
- Detailed descriptions of methods
```

Record the cover-letter format as a fillable skeleton, not prose instructions.

### Title page (for double-blind journals)

Record two lists:

**Elements required on the title page (separate file):**
```
☐ Full article title
☐ All author names (exact order matching the submission system)
☐ Each author's affiliation (department, institution, city, country)
☐ Corresponding author: full postal address + email
☐ Present address (if different from work address — footnote)
☐ Acknowledgements (title page ONLY — not in the manuscript)
☐ [Add any journal-specific fields found in the Guide for Authors]
```

**Elements to strip from the anonymized manuscript:**
```
☐ Author names and affiliations (everywhere in the body)
☐ Acknowledgements (move to title page)
☐ Funding references
☐ Self-citations: replace "we have shown [Author, 2022]" with "[Anonymous, 2022]"
☐ Self-citations in reference list: "[Anonymous, 2022] Details omitted for review"
☐ Institutional identifiers in figures or supplementary material
☐ Document metadata (clear author field in file properties)
```

### Mandatory declarations

For each declaration, note: mandatory or conditional (only if applicable), where it goes in the manuscript, and the standard template wording:

| Declaration | Mandatory? | Where | Template |
|-------------|-----------|-------|----------|
| Competing interest | Always | Separate file / end of MS | "The authors declare no competing interests." or list each |
| CRediT author statement | Always | Separate file / end of MS | List each author's roles from the 14 CRediT roles |
| Data availability | Always | End of MS | State repository + DOI, or reason data cannot be shared |
| Ethics / informed consent | If human subjects | End of MS | State IRB name + approval number |
| Generative AI use | If AI used in writing | Before references | "During preparation, [author] used [tool] to [purpose]. The author reviewed and takes full responsibility for the content." |
| Funding | Always | End of MS | "This work was supported by [Funder] grant [number]." or "No specific funding was received." |

### Format gates (cheapest desk-rejects to avoid)

Record as a checklist:

```
☐ Word limit: ≤[N] words (excluding [references / appendices / highlights])
☐ Abstract: [structured / unstructured], ≤[N] words
☐ Highlights: [3–5] bullets, ≤[N] characters each (including spaces)
☐ Reference style: [APA 7th / Vancouver / etc.]
☐ File format: [.docx single-column / .tex with Elsevier template / no PDF source]
☐ Section numbering: [required: 1, 1.1, 1.1.1 / not required]
☐ Double-blind: [yes / no] — if yes, separate title page required
```

---

## 5. Handling contradictions and change

Journals evolve. Treat contradictions as signal, not error.

**New editor or scope relaunch**: note the transition year; weight recent papers (last 1–2 years) more heavily; state the direction of change explicitly.

**Special issues vs regular issues**: a special issue's topic mix reflects guest editors' interests, not the standing editorial preference. Tag special-issue papers separately and do not let them dominate the topic analysis.

**Contradictions within the corpus**: record both patterns and the conditions under which each appears. Do not average them into a single description.

Example:
```
Fork: Discussion section
- Pattern A (Papers A, C, E): Discussion merged with Conclusion (no separate section)
- Pattern B (Papers B, D): Separate Conclusion restates RQ answers; Discussion is interpretation only
Both are acceptable. Authors can choose; Pattern A is slightly more common (3/5 sampled).
```

---

## 6. Calibration: testing before shipping

Hold out calibration papers *before* finalizing findings (so the test is honest).

**Hit test**: take 2 papers the journal published that you did NOT use to build the profile. Run them through the Stage-1 logic. Both must score SUBMIT. If either fails, the Stage-1 signals are wrong — revise and retest.

**Redirect test**: take 1 paper from the rival journal (or a clearly off-topic paper). Run it through Stage-1. Must score REDIRECT with a specific, correct reason. If it scores SUBMIT, the signals are too broad — tighten them.

Use a subagent for calibration where possible. The same model that built the profile will tend to rationalize its own decisions; an independent checker catches this.

---

## 7. Pre-shipping checklist

Before writing the child skill:

**Signal quality**
- [ ] Every Stage-1 finding passes both the rival-journal test and the prediction test
- [ ] At least one claims-vs-reality gap is named, classified, and turned into either a red flag or an exploitable preference
- [ ] The "this journal vs rival" one-liner would not apply equally if you swapped in the rival's name

**Writing framework**
- [ ] The abstract template is a fill-in skeleton with labeled sentence functions, not a description
- [ ] The abstract template is anchored to at least one real example (with a DOI or source)
- [ ] Title patterns are 2–3 specific patterns with real examples, not "clear and informative"
- [ ] Section structure records the standard sequence AND notes any fork patterns

**Submission kit**
- [ ] Cover letter skeleton has labeled beats + an explicit list of what NOT to include
- [ ] Title page is a checklist (if double-blind: includes the anonymization strip-list)
- [ ] Every mandatory declaration is listed with its placement and template wording

**Calibration**
- [ ] Hit test passed: 2 held-out in-journal papers → SUBMIT
- [ ] Redirect test passed: rival-journal or off-topic paper → REDIRECT

**Honesty**
- [ ] Sample size and research date stated
- [ ] Any inferred or low-confidence items labeled [LOW] or [INFERRED]
- [ ] "Fit improves odds, not a guarantee" in the limits section
- [ ] "Verify against the live Guide for Authors before submitting" in the submission kit
