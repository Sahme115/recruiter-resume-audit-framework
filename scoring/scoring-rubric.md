# Scoring Rubric

A standardized 0–10 rubric for each of the 5 audit dimensions. Designed so that two different reviewers should land within ±1 of each other on the same resume.

This is the most-cited document in the framework. If you only adopt one thing from this repo, adopt this.

---

## How to use

1. Score each dimension 0–10 using the anchors below.
2. Sum to a verdict score out of 50.
3. Map to action via [aggregate-formula.md](aggregate-formula.md).

A machine-readable version of the same rubric: [scoring-rubric.json](scoring-rubric.json).

---

## Dimension 1 — Six-Second Scan

> "Can a recruiter answer 'what does this person do?' in six seconds?"

| Score | Anchor |
| --- | --- |
| 0 | Summary is all adjectives ("passionate, results-driven"). No artifact named on page 1. |
| 3 | Summary names role and years but no stack/domain. Top bullet is buzzword soup. |
| 6 | Summary names role, years, stack. Top bullet has a verb + a vague noun. |
| 9 | Summary names role, years, stack, one specific recent scope. Top bullet has artifact + collaborator. |
| 10 | Plus: the first 1–2 words of every bullet vary, no two are identical. |

---

## Dimension 2 — Credibility

> "Would any bullet collapse on one follow-up question?"

| Score | Anchor |
| --- | --- |
| 0 | Multiple invented metrics or phantom artifacts; scope inflation throughout. |
| 3 | One invented metric or one scope-inflated bullet on page 1. |
| 6 | No clearly invented numbers, but several vague ownership claims ("drove strategic initiatives"). |
| 9 | Every metric has a source. All "Led/Owned" claims are honest. One or two unsurvivable claims remain. |
| 10 | Plus: at least one bullet honestly describes something that went wrong or was decided against. |

---

## Dimension 3 — ATS

> "Will the system parse and match this?"

| Score | Anchor |
| --- | --- |
| 0 | Image-only PDF / scanned. No standard headings. Tables for core content. |
| 3 | Text-selectable PDF but multi-column layout or icon-heavy skills section. |
| 6 | Standard headings, one-column. Some role keywords present but only in a skills dump. |
| 9 | Plus: 8+ role keywords appear inside real bullets. Exact tool names (PostgreSQL, not "SQL databases"). |
| 10 | Plus: zero keyword stuffing, no hidden text, skills section has exact versions where relevant. |

---

## Dimension 4 — Impact vs Activity

> "Did they ship or just attend?"

| Score | Anchor |
| --- | --- |
| 0 | 80%+ activity verbs (Was responsible for, Supported, Helped with). |
| 3 | Mostly activity; one or two impact bullets buried lower. |
| 6 | ~50/50 impact vs activity. Top bullet of recent role is impact. |
| 9 | ~70% impact bullets on page 1. Every impact bullet names an artifact. |
| 10 | Plus: at least one bullet describes a specific decision (kept / killed / replaced). |

---

## Dimension 5 — Tone

> "Does this sound like a human who actually did the work, or like LLM-polished copy?"

| Score | Anchor |
| --- | --- |
| 0 | Symmetric rhythm. Tier-1 buzzwords on every line. Em-dashes everywhere. |
| 3 | Some buzzwords removed; bullets still uniformly 20–25 words. |
| 6 | Mixed lengths; varied lead verbs. 1–2 buzzwords slip through. |
| 9 | Zero Tier-1 buzzwords. One bullet under 14 words; one over 22. No two bullets share lead word. |
| 10 | Plus: one bullet would have been impossible for ChatGPT to write (mentions a real, unusual specific). |

---

## Inter-rater calibration

When training a team of reviewers on this rubric, the standard calibration exercise:

1. Three reviewers score the same five resumes independently.
2. Compute mean and standard deviation per dimension.
3. Investigate any dimension with std > 1.5.

Within-rubric drift past ±1 usually means the anchors aren't being read literally — re-anchor against this document.

---

## See also

- [aggregate-formula.md](aggregate-formula.md) — turning the 0–50 score into a submit verdict
- [Decision tree](../heuristics/decision-tree.md) — fast bullet-level decisions
- [Recruiter audit checklist (PDF)](../downloads/recruiter-audit-checklist.pdf)
- Live tool: [cvpage.org/resume-credibility-checker](https://cvpage.org/resume-credibility-checker)
