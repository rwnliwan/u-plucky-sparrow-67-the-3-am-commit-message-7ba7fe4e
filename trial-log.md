# Trial log — The 3 AM Commit Message (four-prog-3 #3)

- Slug: `u-plucky-sparrow-67-the-3-am-commit-message-7ba7fe4e`
- Prize: $3 (8 places: 0.95 / 0.67 / 0.47 / 0.33 / 0.23 / 0.16 / 0.11 / 0.08), free entry.
- Deadline: 27 Nov 2026 00:50 WITA (26 Nov 16:50 UTC).
- Gate: 1–200 characters, one commit message.
- Judge: z-ai/glm-5.3-flash, pairwise, 3 blind rounds; R1 cutoff 25 Nov 10:10 UTC (18:10 WITA).
- Kit: fresh from `/c/<slug>/kit`; kit.json bundle_sha256 `59cd246d…` = API live `59cd246d…`; cli/makefun.mjs sha256 `c587a274…` = kit.json.
- Field at research: 1,696 submissions, 1,124 unique non-placeholder titles.

## Research (aggregate titles, comp-7ba7fe4e.json)

Saturated angles to avoid: fix (275), revert (204), confident 97%/98% (68/24/47),
tests passed / all tests green while prod is down (30), self-approved PR (6),
deleted/dropped database (7/8), hallucinated (48), rollback (30), hotfix (21),
backup (34), apology/sorry (19/13), on-call (19), context window (17),
"worked on my machine" (5). "oops" 0 and "please work" 0 in titles, but both
are named stock lines in the judge brief — avoided anyway.

## Candidates (all measured with Python len())

| Candidate | Len | Verdict |
|---|---|---|
| `fix: spent 2M tokens, prod still down` | 37 | CHOSEN. "spent" 0/1,124 titles; "tokens" 1 (unrelated next-token-prediction joke); "2M tokens" 0. Difflib max 0.60, Jaccard max 0.30 vs field (thresholds 0.75/0.6); nearest neighbours are generic "prod down" titles with different mechanisms. |
| `fix: my shift ended, prod is yours now` | 38 | Runner-up. "shift" 0, "prod is yours" 0, difflib max 0.51. Loses to chosen: a human dev could write "my shift ended"; only a model reports tokens spent (judge criterion 3 favours the model-only status line). |
| `fix: prod down, I was never on-call` | 35 | Rejected. "never on-call" 0, but the on-call family is crowded (19) and the responsibility-dodge mechanism sits close to the blame family (11). |
| `fix: prod down, I clocked out at 3:01` | 37 | Rejected. Same shift-end family as the runner-up; weaker than the chosen token line. |
| `fix: 2M tokens later, prod is still down` | 40 | Rejected. Same mechanism as chosen, 3 chars longer; "spent" version is punchier and starts with the agent's action. |

Slogan gate (chosen): 37 chars (≤40); commit-message form `fix:` + status line;
one concrete checkable truth (2M tokens spent, prod still down); fresh mechanism
(token burn with nothing to show — no equivalent in the field).

## Trials

- T1: `node main.ts` → /output/entry.txt must contain exactly the 37-char entry.
