# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/73

**Verdict output**

I'll invoke the issue-select skill to grade these against the rubric.

● Skill(issue-select)
Successfully loaded skill

I'll read the skill's rubric and scope files first.

Read 3 files, listed 1 directory, ran 8 shell commands

All three URLs are inside the scoped repo (codepath/pathreview-ai301-fa26-s1). Graded each independently against the three required checks in rubric.md.

Shared repo evidence: pushed_at: 2026-09-16T21:48:27Z (6 days before today), archived: false; collaborator Aburke225 first-replied in 6 days on both #52 and #43. Only one PR exists in the whole repo (#74, against issue #60), so no PR touches any of these three.

Accepted, in order:

#73 — README / .env.example disagree about the LLM API key
Community alive — pass: last push 2026-09-16, 6 days ago.
Scope fits — pass: names README.md and .env.example, says core/config.py defines both keys, "Make the two files agree"; labeled good first issue by COLLABORATOR Aburke225.
Unclaimed — pass: assignees: [], zero comments, no PR.
Why first: the only candidate with nobody else on it, and the smallest stated effort (1–2 hours).
#69 — Output parser crashes on a top-level JSON array
Community alive — pass (same repo evidence).
Scope fits — pass: names rag/generator/output_parser.py + its test, describes the exact AttributeError and the xfail marker (H-02) to remove.
Unclaimed — pass: assignees: []; jacho15 commented "I'd like to attempt this!" but is author_association: NONE — a classmate, which the Path Review house rule says does not block. No PR.
#68 — Keyword search ZeroDivisionError on empty index
Community alive — pass (same repo evidence).
Scope fits — pass: names rag/retriever/keyword_search.py + its test, the BM25Okapi cause, and the H-01 xfail marker to remove.
Unclaimed — pass: assignees: []; yulijasso ("I'd like to take this bug") is author_association: NONE, and the two referenced events point at commits in yulijasso/ai301-coursework, a personal repo — not a PR against this repo. House rule: does not block.

Two notes. The fit profile section of scope.md is still the placeholder (Write a few sentences here.), so I could not rank by fit as the skill intends — the order above uses duplication and stated effort as an explicit stand-in. And #68 already carries a full reproduction plus a detailed implementation plan from a classmate; it costs you nothing under the house rule, but it's the most duplicated of the three.

[
{
"item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/73",
"checks": [
{"name": "Community alive", "grade": "pass", "evidence": "repo pushed_at 2026-09-16T21:48:27Z, 6 days before capture date 2026-09-22 (<60); also collaborator Aburke225 first-replied in 6d on #52 and #43 (<7)"},
{"name": "Scope fits a newcomer", "grade": "pass", "evidence": "body names README.md and .env.example and the settled direction 'Make the two files agree'; labeled 'good first issue' by COLLABORATOR Aburke225"},
{"name": "Unclaimed", "grade": "pass", "evidence": "assignees: [], 0 comments, no linked or referenced PR (repo's only PR #74 targets issue #60)"}
],
"verdict": "accept"
},
{
"item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/69",
"checks": [
{"name": "Community alive", "grade": "pass", "evidence": "repo pushed_at 2026-09-16T21:48:27Z, 6 days before capture date 2026-09-22 (<60)"},
{"name": "Scope fits a newcomer", "grade": "pass", "evidence": "body names rag/generator/output_parser.py and tests/unit/test_output_parser.py, the AttributeError cause, and the H-02 xfail marker to remove; labeled 'good first issue' by COLLABORATOR"},
{"name": "Unclaimed", "grade": "pass", "evidence": "assignees: []; jacho15's 'I'd like to attempt this!' is author_association NONE (classmate, non-blocking per Path Review house rule); no linked PR"}
],
"verdict": "accept"
},
{
"item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/68",
"checks": [
{"name": "Community alive", "grade": "pass", "evidence": "repo pushed_at 2026-09-16T21:48:27Z, 6 days before capture date 2026-09-22 (<60)"},
{"name": "Scope fits a newcomer", "grade": "pass", "evidence": "body names rag/retriever/keyword_search.py and tests/unit/test_keyword_search.py, the BM25Okapi divide-by-zero, and the H-01 xfail marker to remove; labeled 'good first issue' by COLLABORATOR"},
{"name": "Unclaimed", "grade": "pass", "evidence": "assignees: []; yulijasso's claim is author_association NONE (classmate, non-blocking per house rule); both 'referenced' events are commits in yulijasso/ai301-coursework, not a PR to this repo"}
],
"verdict": "accept"
}
]


---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

1. First graded run (after fixing a Windows Unicode/subprocess encoding issue in the harness): 14/20 scored items agree, below the 18 bar. Every disagreement traced to the "Scope fits a newcomer" check failing well-specified multi-file issues.
2. Revision attempt: loosened the Scope check's pass condition, but an editing error also accidentally deleted the "Unclaimed" check row from the table. Result: 9/20 scored items agree, with claimed 0/4 and policy 0/1.
3. Final run: restored the Unclaimed check row alongside the loosened Scope check. Result: 16/20 scored items agree, with every category meeting the floor (claimed 4/4, clear-accept 4/8, dead-repo 3/3, policy 1/1, scope 4/4).

**Issue analysis**

issue-01 (conda/conda#16475): gold label is accept, and my rubric's final verdict is accept (agree). This issue initially failed my rubric's "Scope fits a newcomer" check, because that check originally required a single named file or function with one bounded fix. issue-01 actually proposes a well-specified plan spanning multiple documentation files (a new task page plus edits to three existing pages), which is concrete and actionable but not single-file. I revised the Scope check to accept any concrete, actionable plan naming specific file(s)/page(s), not just a single file, which correctly flipped this issue to accept.

**Check rationale**

"Scope fits a newcomer | issue body, comment thread, labels, and author_association | Issue lays out a concrete, actionable plan (specific file(s)/page(s)/function(s) and what the change should contain), OR is labeled "good first issue" (or similar) and opened/endorsed by a maintainer or collaborator; fails if it is an open request or unresolved design debate with no settled direction and no such label | required"

I wrote this check to catch the difference between issues that give a newcomer a clear, boundable task and issues that are still open design questions. I widened it from a single-file requirement to multi-file plans after finding a real issue (issue-01) that was well-specified but spanned several files, and I added the "good first issue" label as a second path to passing because a maintainer explicitly flagging an issue as approachable is real evidence of scope, even when the issue body itself is terse.

**Trade-offs**

Adding the "good first issue" label as an alternate path to passing Scope means my rubric now trusts a repo's own labeling in place of reading a terse issue body closely. This correctly flipped issue-04 (a short bug description on zxcalc/zxlive, labeled "good first issue" by a collaborator) to accept. The trade-off is that my rubric could now accept an issue that is genuinely underspecified if a maintainer mislabels it "good first issue," since the label overrides the requirement for a concrete written plan. My rubric still disagrees with the gold labels on about 4 of the 20 scored issues, all failing Scope, which are likely issues with real merit that are simply shorter and less structured than what my check rewards.

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

1. This issue (a README/.env.example key-name mismatch) fits my available time well — my own skill's output estimated a 1-2 hour effort, which is realistic alongside my coursework and job.
2. My skill's verdict correctly identified that this issue has no assignee, no linked PR, and zero competing interest from classmates, unlike the other two candidates I ran, both of which had a classmate express interest in the comments (non-blocking under the house rules, but still worth weighing). What the rubric alone couldn't tell me is which of the three accepted issues I'd personally find most approachable to start with — I picked the smallest-scoped one as a first issue.
3. I anticipate low difficulty in claiming it — the fix is narrowly scoped to reconciling two files that already state conflicting environment variable names, so there's little ambiguity about what "done" looks like, and no one else appears to be working on it.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
