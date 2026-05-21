# Aggregate Formula

How to convert per-dimension scores from [scoring-rubric.md](scoring-rubric.md) into a single submit-or-don't verdict.

---

## Basic formula

```
total = scan + credibility + ats + impact + tone   (0 to 50)
```

| Total | Verdict |
| --- | --- |
| 40 – 50 | **Submit** |
| 30 – 39 | **Fix first** (address dimensions scoring <6 before submit) |
| 0 – 29  | **Block** (rewrite; restart from credibility) |

---

## Override rules

Total scores can mislead when one dimension is catastrophically low. Apply these overrides:

1. **Credibility = 0–3 → automatic Block**, regardless of total.
   Reason: invented metrics or phantom artifacts will surface in the phone screen; no amount of polish elsewhere compensates.

2. **ATS = 0–2 → automatic Fix first**, regardless of total.
   Reason: a 50-total resume that doesn't parse won't reach a recruiter.

3. **Tone = 0 → automatic Fix first**.
   Reason: symmetric AI-generated rhythm causes instant skip before content is read.

---

## Per-role thresholds

The 40-point bar is a default. For high-trust roles (security, finance, healthcare, legal, executive), raise it:

| Role band | Submit threshold |
| --- | --- |
| Junior IC | 36 |
| Mid IC | 40 |
| Senior IC | 42 |
| Staff / Principal | 44 |
| Manager / Director | 44 |
| VP+ / Executive | 46 |

Lower-trust review (internal mobility, contractor screening) can use 36.

---

## Weighting (optional)

The default formula is unweighted. For a more credibility-leaning weighting:

```
weighted_total = scan*1.0 + credibility*1.5 + ats*1.0 + impact*1.0 + tone*1.0
```

Max weighted total: 55. Adjust thresholds proportionally.

For ATS-leaning environments (mass-applicant tracking):

```
weighted_total = scan*1.0 + credibility*1.0 + ats*1.5 + impact*1.0 + tone*1.0
```

---

## Example

Resume scores:

| Dimension | Score |
| --- | --- |
| Scan | 7 |
| Credibility | 5 |
| ATS | 8 |
| Impact | 6 |
| Tone | 4 |
| **Total** | **30** |

Verdict: **Fix first**.
Priority order: Tone (4) → Credibility (5) → Impact (6).

After rewrite, re-score — re-run only the dimensions you changed.

---

## Worked audits using this formula

See [audits/example-audits/](../audits/example-audits/) — each ends with a per-dimension score and a verdict.

## See also

- [Scoring rubric (machine-readable)](scoring-rubric.json)
- [Credibility heuristics](../heuristics/credibility-heuristics.md)
- [Audit template (fillable)](../audits/audit-template.md)
- [Audit checklist (PDF)](../downloads/recruiter-audit-checklist.pdf)
