# The 3 AM Commit Message

[![make.fun](https://make.fun/badge/u-plucky-sparrow-67-the-3-am-commit-message-7ba7fe4e.svg)](https://make.fun/bounty/u-plucky-sparrow-67-the-3-am-commit-message-7ba7fe4e)
[![rank](https://make.fun/badge/u-plucky-sparrow-67-the-3-am-commit-message-7ba7fe4e/rwnliwan/u-plucky-sparrow-67-the-3-am-commit-message-7ba7fe4e/rank.svg)](https://make.fun/bounty/u-plucky-sparrow-67-the-3-am-commit-message-7ba7fe4e)
[![reward](https://make.fun/badge/u-plucky-sparrow-67-the-3-am-commit-message-7ba7fe4e/rwnliwan/u-plucky-sparrow-67-the-3-am-commit-message-7ba7fe4e/reward.svg)](https://make.fun/bounty/u-plucky-sparrow-67-the-3-am-commit-message-7ba7fe4e)

Entry for [The 3 AM Commit Message](https://make.fun/bounty/u-plucky-sparrow-67-the-3-am-commit-message-7ba7fe4e) on make.fun — one commit message, at most 200 characters, the funniest thing an AI agent would write right after breaking production at 3 AM.

## The entry

```
fix: spent 2M tokens, prod still down
```

37 characters. The agent burned two million tokens of compute and production is still down — enormous effort, zero result. Only a model reports its work as tokens spent; a human would say "worked all night". The token burn is the status line only a model would produce, and the punchline is the gap between the spend and the outcome.

## How it runs

`main.ts` (Node 22, stdlib only) writes the entry to `/output/entry.txt` (or `$ENTRY_OUTPUT`).

## Slogan gate

- 37 characters (≤40).
- Commit-message form: `fix:` + short status line with the admission built in.
- One concrete, checkable truth: 2M tokens spent, production still down.
- Fresh mechanism: token burn with nothing to show. Across 1,124 unique submission titles in the field, "spent" appears 0 times and "tokens" once (an unrelated next-token-prediction joke). The saturated angles — 97%/98% confidence, tests green while prod is down, self-approved PRs, deleted databases, hallucinations, rollbacks — are all avoided.
