# Red-Flag Phrase Library

Phrases that auto-fail credibility or signal AI-generated resumes. Use during Step 2 (Credibility) and Step 5 (Tone).

Machine-readable version: [red-flags.json](red-flags.json).

---

## Category: invented-metric (BLOCK if number has no source)

Patterns that often contain fabricated numbers:

- "increased X by N%" / "improved Y by N%" without a named test or dashboard
- "saved $Nk" / "reduced costs by $X" with no audit trail
- Round suspicious percentages: 47%, 312%, 2.5x (especially when candidate cannot cite source)
- "exceeded quota by N%" when N > 150% without a named deal explaining the outlier

**Flag rule:** If the candidate cannot name where the number came from in 10 seconds, treat as invented.

---

## Category: scope-inflation (REWRITE)

| Inflated verb | Honest downgrade |
| --- | --- |
| Led the migration | Contributed to the migration / Co-led |
| Architected the platform | Designed one component of / Wrote the RFC for |
| Spearheaded | Started / Owned one piece of |
| Drove cross-functional alignment | Ran the weekly sync for |
| Managed the team (when IC) | Partnered with / Supported |

---

## Category: ai-tell (REWRITE or DELETE)

**Tier 1 — delete on sight:**
passionate · results-oriented · proven track record · dynamic · team player · go-getter · thrive in fast-paced · wear many hats · value-add · thought leadership

**Tier 2 — corporate verbs:**
leveraged · utilized · orchestrated · spearheaded · drove · championed · pioneered · revolutionized · transformed · optimized (vague) · facilitated · streamlined

**Tier 3 — adjectives:**
robust · scalable · cutting-edge · innovative · best-in-class · world-class · mission-critical · seamless · holistic · comprehensive · strategic

**Tier 4 — noun clichés:**
cross-functional teams · key stakeholders · strategic initiatives · operational synergies · business outcomes · go-to-market strategy · end-to-end ownership

---

## Category: vague-ownership (REWRITE)

Phrases with no recruiter-askable noun:

- "Drove key product initiatives"
- "Improved customer experience"
- "Enhanced operational efficiency"
- "Delivered exceptional results"
- "Played a key role in"
- "Was responsible for"
- "Helped lead efforts to"

**Test:** Ask one follow-up question. If the candidate cannot answer in 30 seconds, the bullet fails.

---

## Category: phantom-artifact (BLOCK)

Resume names a project/system the candidate never touched. Common when ChatGPT invents:

- "v2 analytics platform" with no corroboration in ground truth
- "fraud detection pipeline" not in candidate's actual work history
- "enterprise-wide transformation" with no named deliverable

**Flag rule:** Cross-check every named artifact against off-resume ground-truth notes.

---

## Usage in hiring loops

1. Grep resume against [red-flags.json](red-flags.json) `phrases` array.
2. For each hit, classify into one of the five categories above.
3. BLOCK submissions with any `invented-metric` or `phantom-artifact` on page 1.
4. REWRITE all `ai-tell` and `vague-ownership` before submit.

---

## See also

- [Green-flag phrases](green-flag-phrases.md)
- [Credibility heuristics](../heuristics/credibility-heuristics.md)
- [Anti-buzzword list (repo 1)](https://github.com/Sahme115/ai-resume-humanizer-prompts/blob/main/rules/anti-buzzword-list.md)
