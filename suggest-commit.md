---
description: Suggest a commit message for staged changes
---

I have staged changes and need a commit message suggestion.

Review what's staged by running:
- `git diff --cached --stat` — summary of staged files
- `git log --oneline -5` — recent commit style reference

If needed, dig deeper with `git diff --cached`.

Suggest a message in Conventional Commits format (`type(scope): description`). Use a body when there's useful context, and scope when it's clear. Don't stage, commit, or modify anything — just suggest.
