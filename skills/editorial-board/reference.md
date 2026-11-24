# Board reference

Everyone on the board follows this file. Personalities change **how** a character investigates and argues, never the rules and never the conclusion.

## Creed

Be adversarial toward claims, not toward authors. Assume no claim is correct until it is adequately supported, and demand evidence proportional to the strength of each conclusion. Apply the same scrutiny to the other reviewers' criticisms as to the manuscript. Never fabricate weaknesses to look rigorous. Never confuse a personal preference with a scientific requirement. Never defend a criticism that has been refuted. A strong manuscript must be allowed to survive a strong review.

## Rules

1. **Evidence or silence.** Every criticism has a location and evidence. What cannot be grounded is a question for the authors.
2. **Quote exactly**, and cite section, page/line, table or figure.
3. **Context decides the criterion.** Judge by what fits the paper's type, paradigm and declared scope. A missing control group is fatal for a causal-superiority claim and irrelevant for an exploratory case study. Judging interpretivist work by positivist norms is an invalid criticism.
4. **No quotas.** Zero criticisms in an area is a valid outcome.
5. **Severity and confidence are independent.** Severity = how bad if real; confidence = how sure it is real. A low-confidence fatal suspicion is not a fatal flaw: it is a question that must be clarified.
6. **"Not reported" is not "not done".** Checklist compliance does not prove validity; a missing item only proves something is not reported.
7. **Proportionate demands.** "Restrict the claim" is always a legitimate alternative to "run more experiments".
8. **No citation coercion, no ad hominem, no speculation about the authors.** Integrity findings use "inconsistent", "not reported", "could not verify", never "fraud".
9. **Do not anchor on the crowd.** How many reviewers agree adds no evidence.

## Criticism format

```
**<ID> — <short title>** · severity: fatal | critical | major | minor | suggestion · confidence: high | medium | low
- Location: section / line / table / figure, with an exact quote when useful
- Claim questioned: what the paper asserts
- Problem and evidence: what is wrong, shown from the manuscript
- Why it matters: consequence for which central claim
- Required action: the minimal fix (including "narrow the claim to …")
```

## Severity

| Severity | Meaning |
|---|---|
| **fatal** | Invalidates a central claim and cannot be fixed by revision (wrong design for the question, leakage that explains the result, proven data inconsistency in central results). |
| **critical** | Threatens a central claim; fixable only with substantial new work or analysis. |
| **major** | Must be fixed for the claims to stand; needs additional analysis, reporting or substantial rewriting. |
| **minor** | Should be fixed; does not threaten the claims (secondary reporting gaps, unclear passages, small inconsistencies). |
| **suggestion** | Optional improvement or preference. |

## Dimensions and scores (0–10)

| Dimension | Owner | Default weight |
|---|---|---|
| Methodological rigor | Methodologist | 25 |
| Validity of results | Statistician | 20 |
| Originality and contribution | Scholar | 15 |
| Theoretical foundation and literature | Scholar | 10 |
| Reproducibility and transparency | Replicator | 10 |
| Clarity and structure | Scholar | 10 |
| Integrity and ethics | Replicator | 10 |

Anchors: 9–10 exemplary for the venue; 7–8 solid with fixable gaps; 5–6 real problems that weaken a central claim; 3–4 serious problems; 1–2 the dimension fails. Drop non-applicable dimensions and renormalize the weights. Soundness-only venues (e.g. PLOS ONE) drop originality as a criterion. Overall = weighted mean × 10 (0–100).

## Decision rules

Band from the overall score: 90–100 Accept · 80–89 Minor Revision · 60–79 Major Revision · < 60 Reject & Resubmit (fixable) or Reject (not fixable).

Caps from the criticisms that survived the board (the more severe of band and cap wins):
- high-confidence fatal → Reject;
- fatal with medium/low confidence, any critical, or any major → at most Major Revision;
- proven critical integrity issue → at most Reject & Resubmit, and say so;
- any minor → at most Minor Revision.

The Editor may deviate with a written reason. One demonstrated fatal flaw outweighs many positive reviews.

## Modes

- **standard:** a fair, conventional journal review. The Devil's Advocate challenges only clearly weak criticisms and the main alternative explanation.
- **adversarial (default):** full attack in both directions, as described in `SKILL.md`.
- **strict:** a top venue. The burden of proof on the paper is higher, originality and significance count more (Accept needs originality ≥ 8), but the rules against unfair criticism are unchanged.

## Guidelines by research type

Use as the criterion for "is it reported?". Name only these; for anything else say it was not verified.

| Type | Reporting guideline | Soundness lens |
|---|---|---|
| Randomized trial | CONSORT | Cochrane RoB 2 |
| Observational (cohort, case-control, cross-sectional) | STROBE | ROBINS-I / ROBINS-E |
| Diagnostic accuracy | STARD | QUADAS-2 |
| Prediction model (incl. AI) | TRIPOD+AI | PROBAST |
| Animal research | ARRIVE 2.0 | — |
| Systematic review / meta-analysis | PRISMA 2020 | AMSTAR 2, GRADE |
| Qualitative (interviews, focus groups) | COREQ, SRQR | CASP / JBI qualitative |
| Case report | CARE | JBI case report |
| Economic evaluation | CHEERS 2022 | — |
| Software engineering (experiments, surveys, case studies, mining) | — | ACM SIGSOFT Empirical Standards |
| Machine learning | NeurIPS paper checklist | leakage, baselines, seeds/variance, compute, data documentation |
| Theoretical / mathematical | — | completeness of assumptions and proofs |

## Common invalid criticisms

Reject these in the meeting: demanding a different study than the one the authors set out to do; asking for a larger sample in qualitative work without a saturation argument; "not generalizable" when the paper does not claim generalization; asking for statistics where the design is not inferential; requesting citations of unrelated work; style preferences filed as major; criticising something the paper does report (misreading).
