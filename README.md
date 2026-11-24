# Reviewers Against You

A Claude Code plugin that puts your manuscript in front of a hostile but fair editorial board **before** you submit it.

> Every claim in the manuscript must survive the board, and every criticism the board raises must survive the other reviewers.

Inspired by [interviewers-against-you](../interviewers-against-you), applied to academic peer review.

## The board

| Character | Leads on |
|---|---|
| **The Methodologist** | Design, validity, sampling, bias, ethics approvals |
| **The Statistician** | Analysis, effect sizes, uncertainty, data consistency |
| **The Scholar** | Originality, literature, theory, relevance, clarity and claim drift |
| **The Replicator** | Reproducibility, transparency, disclosures, integrity |
| **The Devil's Advocate** | Attacks the paper's claims *and* the reviewers' criticisms |
| **The Editor** | Runs the debate, rules on each criticism, decides |

## How a session runs

1. **Intake.** The Editor reads the manuscript and writes a brief: research type, central claims and their strength, applicable reporting guideline (CONSORT, STROBE, PRISMA, COREQ, SIGSOFT Empirical Standards, NeurIPS checklist…).
2. **Independent review.** The four reviewers review in parallel, each in their own subagent, without seeing each other. The Scholar searches the web to check that the key references exist, match their metadata, are not retracted and support what they are cited for, and looks for close prior work the paper does not cite.
3. **Board meeting.** The Devil's Advocate challenges weak, exaggerated or unfair criticisms and the paper's main result; reviewers defend, reformulate or withdraw; the Editor rules on each one.
4. **Decision.** Only the criticisms that survived count: dimension scores, overall score, decision (Accept / Minor / Major / Reject & Resubmit / Reject) and a P0–P3 roadmap.

## Install

```
/plugin marketplace add <path-or-repo-of-this-plugin>
/plugin install reviewers-against-you@reviewers-against-you
```

## Use

```
/reviewers-against-you:editorial-board paper.pdf
/reviewers-against-you:editorial-board paper.md "PLOS ONE" standard
/reviewers-against-you:editorial-board paper.tex NeurIPS strict quick
```

- **venue** (optional): a journal or conference; its criteria are applied when known.
- **mode**: `standard`, `adversarial` (default) or `strict`.
- **offline**: no web access; references and prior work are not checked online.
- **quick**: no subagents; the main session writes the four reviews itself. Cheapest option.
- Write in Portuguese (or any language) and the whole session follows it.

Output goes to `editorial-board/<date>-<slug>/`: `brief.md`, `reviews.md`, `debate.md`, `report.md`. That folder is git-ignored because it contains your unpublished manuscript's content.

After the report, you can paste the authors' rebuttal and the board reconvenes for one round.

## Cost

A full session runs four reviewer subagents, each reading the whole manuscript once, plus the main session. The Scholar's literature search adds about 10–25 web searches. With `quick`, there are no subagents at all. There is no multi-round debate between agents: the meeting is written by the main session from the four reviews.

## Limits

This is a simulation, not an editorial decision. The literature search only sends public data to the web (the cited works' titles, authors, DOIs and generic topic terms), never your manuscript's text, title or results; use `offline` to avoid the web entirely. References it could not check are marked "not verified". It does not run your code or data.

## License

MIT
