# 18F/charlie context
> refreshed 2026-09-05 | upstream default: main @ 6793fdf

## Identity & policies
- upstream: 18F/charlie, default branch main, primary language JavaScript (Node/Slack Bolt)
- English-first: yes (all docs/issues/README in English)
- CLA/DCO: none. CONTRIBUTING waives copyright to CC0 public domain on PR submission; no CLA bot, no DCO sign-off required.
- AI-assisted PR policy: unstated (no mention in CONTRIBUTING, README, or org 18F/.github)
- signed commits required: no (from CONTRIBUTING / branch protection)
- PR template: yes — `.github/pull_request_template.md` (fill verbatim)
- external tracker: github

## Conventions (verified from merged PRs)
- branch naming: mixed human styles (`fix/...`, `aj/...`, `ap-...`, `update-...`, `margolis-...`); no dominant single pattern. Fall back to `type/kebab-desc`.
- commit style: mixed; short imperative/conventional sentences, merges via squash with `(#NNN)` (dependabot bot merges dominate recent history). Human commits are short plain sentences.
- test command: `npm test` (jest). lint: `npm run lint` (eslint). format: `npm run format-test` (prettier). CI on PRs runs lint + format + jest (reusable_test.yml).
- how outside PRs get merged: historically via maintainers; repo is 18F-maintained, CODEOWNERS = @18F/charlie-maintainers.

## Maintainer picture
- active maintainers: mgwalker is the most visible (commenter on issues/PRs). TTS/18F volunteer team, no guaranteed SLA.
- areas actively worked: mgwalker has in-flight PR #528 on `src/scripts/inclusion-bot.js` (+ its test) — AVOID inclusion-bot.js.

## Issue-area health
- open issues are stale/low-engagement: #295 (Moment migration — maintainer explicitly said "hold on this"); #348 (compound acronym bot, feature idea, no commitment); #375 (bot idea); #555 (inclusion categories, 0 comments); #465, #458 (infra ideas, 0 comments). No small maintainer-engaged open bug suitable for a pick.
- => fall back to repo-audit self-found gap for this run.

## Gap ledger (dedupe — READ FIRST, never re-pick)
- (none yet for this repo)

## Mined gaps (discovered, not yet attempted)
- 2026-09-05 tests/ci `dot-gov.js` `narrowResultsByEntity` entity-filter branches (County, Judicial, Legislative, Federal combined, Independent Intrastate, Interstate, Tribal) are uncovered; existing dot-gov.test.js only covers City and Executive/Executive-branch filters. Proposed: extend the existing "filters correctly by entity" describe with per-type cases using the existing mockCache. Dedupe: no upstream issue/PR covers this. — status: proposed
