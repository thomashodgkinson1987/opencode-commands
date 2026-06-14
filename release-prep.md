---
description: Prepare release notes by drafting description.md from recent commits
---

Let's prepare release notes for the next version.

1. Find the last release tag:
   `gh release list --limit 1 --json tagName --jq '.[0].tagName'`
2. Collect commits since that tag:
   `git log --oneline <last-tag>..HEAD`
3. Increment the patch version (e.g. v0.0.7 -> v0.0.8)

Write `description.md` with a "## What's New" section (user-friendly summary grouped by category) and a "## Changelog" section (commits in conventional
format). Don't include a compare/changelog link.

**Important:** The example below is minimal -- don't truncate or over-summarize to match it. Always capture the full scope of changes since the last release.

Example output:

```
## What's New

- Added publish_release.sh -- automated build and release pipeline...

## Changelog

- chore(gitignore): unignore publish_release.sh for version control
- feat(ci): add publish_release.sh build and release automation script
```

Tell me when `description.md` is ready so I can review it.
