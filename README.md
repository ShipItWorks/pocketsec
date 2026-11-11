# PocketSec

Find out how hackable you are. The scan runs in your browser; what leaves the device is not yet traced (the password check sends a 5-character hash prefix to Have I Been Pwned).

**Score: 56 / 100** on our own [rubric](https://shipitworks.com/how-we-score/). Stage: Alpha. Scored 2026-11-10; this record was updated 2026-11-10 from the [product page](https://shipitworks.com/apps/#pocketsec).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Web (static site). Android wrapper planned; not on Google Play.

## What works today

- Shield Score + grade; demo = 66/C (CLAUDE.md claim) (Tested with sample data)
- Static site builds and prerenders (Tested with sample data)
- Live site reachable (Tested with sample data)

## Not done yet

- Device check AUTO-1..5 (30 pts) (Not tested yet)
- Habits audit HAB-1..6 (70 pts) (Not tested yet)
- HIBP k-anonymity password check (Not tested yet)
- PDF report (Not tested yet)
- The web device check (AUTO-1..5), the habits audit (HAB-1..6), the password check and the PDF report have proof logs on main at 2a92ead (proof/device-check.log, habits-audit.log, breach-prefix-only.log, pdf-report.log), but each records a run at d26a15f, a commit that is not an ancestor of main after the squash merge of #104, so none is credited; headless Chromium on Linux, not the live site or a phone
- Shield Score, the build and the live site are each half credit: the score and live-site logs on main (proof/score-and-demo.log, proof/live-site-trace.log) record runs at commits that are not ancestors of main, and the build has a CI run but no proof log
- What leaves the device is not yet traced at a commit on main: proof/network-trace.log and proof/live-site-trace.log on main record browser-level requests at d26a15f and 9355eb6, which are not ancestors of main (packets and DNS not captured); the README at af82be6 (2026-11-08) said a no-transmission claim for the password
- AUTO-5 menu-path wording changed (#88), but its check script does not pass on Android and no log is committed
- No TWA or AAB; assetlinks.json still holds REPLACE_WITH_ placeholders; the Play 12x14 closed-test rule applies
- LICENSE.md is PolyForm Noncommercial while the plan says All rights reserved - mismatch unresolved
- No CSP header (vercel.json on main at 2a92ead); a /privacy page is on main (src/app/privacy/page.tsx) but no run at a commit on main checks it; contrast, keyboard and TalkBack not checked at a commit on main; dark theme is fixed with no light mode
- Native fix-text Settings paths: at af82be6, proof/native-fix-paths.log recorded 4 of 5 found on a stock Android 36 emulator, 1 not found (Software update), exit 1 (2026-11-08T06:14:48Z); the log on main at 2a92ead records exit 0 for 8 paths at commit 5fdf4a1, which is not an ancestor of main, so it is not credited; an emulator, not a phone
- CHANGELOG.md on main still says there are no release tags (tags v0.1.0 to v0.6.0 exist); package.json says 0.1.0
- At af82be6 (2026-11-08) package.json had no web test script; on main at 2a92ead it has "test": "vitest run" and CI run 42913495225 ran it, but no web test log at a commit on main is committed; proof/native-unit-tests.log on main records 67 native engine tests at 171bc41, not an ancestor of main, on a Linux JVM, not a phone

## What changed

- 2026-11-10: Site copy only: the planned target 'A free score with published rules' now says a top score does not mean the phone is safe. No code or score change.
- 2026-11-10: Land PR #104 merged into main as 2a92ead (6 lane PRs included); no feature label changed this round. Tagged v0.6.0 at 2a92ead.
- 2026-11-08: Native password-check copy now names the host it contacts (api.pwnedpasswords.com) and says the check shows your IP address to Have I Been Pwned; 4 source-reading tests added, 43 native tests pass on a JVM (#44). A run recorded that the habit-fix third-party phrases match six vendor pages, 6 of 6 (#43). A run on a stock Android 36 emulator found 4 of 5 native Settings paths; one not found, run exited 1 (#51). Release v0.5.0.
- 2026-11-08: Two sentences no source backs were dropped from the habit summaries and the web password text, web and native (#62). Release v0.5.0.
- 2026-11-08: Notes only: FOUND.md and LEARNINGS.md additions (#40). No app change.
- 2026-11-08: Menu paths in the device-check fix steps now match the screens on Chrome for Android and Android 16, and a script to check them was added (#88). The script's Android step does not pass yet and no log is committed. Release v0.4.0.

See [CHANGELOG](CHANGELOG.md).

## Demo

[Transcript of the demo (1:56)](https://shipitworks.com/pocketsec/transcript/) · video on the [product page](https://shipitworks.com/apps/#pocketsec)

The demo voice is AI-generated (ElevenLabs, "Alice") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README and a CHANGELOG, and soon a LICENSE. Until the source is public, the [product page](https://shipitworks.com/apps/#pocketsec) is the source of truth, and the score above is the one to trust.

## How we work

Say only what we can back. Say what is not finished before anyone asks. Name people, companies and tools to give credit. Collect as little data as possible. We use AI and say so: Claude (by Anthropic) helps write the code and wrote this README.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02. Owner review by Robert Sweetman: pending.
