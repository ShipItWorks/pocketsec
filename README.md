# PocketSec

Find out how hackable you are. The scan runs in your browser; what leaves the device is not yet traced (the password check sends a 5-character hash prefix to Have I Been Pwned).

**Score: 56 / 100** on our own [rubric](https://shipitworks.com/how-we-score/). Stage: Under 60 (alpha). Scored 2026-11-08; this record was updated 2026-11-08 from the [product page](https://shipitworks.com/apps/#pocketsec).

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
- The web device check (AUTO-1..5), the habits audit (HAB-1..6), the password check and the PDF report have no test or proof log on the main branch; the web test suite and browser run of 2026-11-01 are on a branch that is not merged
- Shield Score, the build and the live site are each half credit: a recorded run exists, but no proof log for them is on main
- What leaves the device is not yet traced: no network capture is on main; the README on main says a no-transmission claim for the password and the page says '60-Second Security Scan' (not measured)
- AUTO-5 menu-path wording changed (#88), but its check script does not pass on Android and no log is committed
- No TWA or AAB; assetlinks.json still holds REPLACE_WITH_ placeholders; the Play 12x14 closed-test rule applies
- LICENSE.md is PolyForm Noncommercial while the plan says All rights reserved - mismatch unresolved
- No CSP header; no privacy page on main; contrast, keyboard and TalkBack not checked; dark theme is fixed with no light mode
- Native fix-text Settings paths: 4 of 5 found on a stock Android 36 emulator, 1 not found (Software update), exit 1 (proof/native-fix-paths.log, 2026-11-08T06:14:48Z); not a phone
- CHANGELOG.md on main still says there are no release tags (tags v0.1.0 to v0.5.0 exist); package.json says 0.1.0
- Web code has no test script in package.json; the only test run on main is the 43 native engine tests, on a Linux JVM, not a phone

## What changed

- 2026-11-08: Native password-check copy now names the host it contacts (api.pwnedpasswords.com) and says the check shows your IP address to Have I Been Pwned; 4 source-reading tests added, 43 native tests pass on a JVM (#44). A run recorded that the habit-fix third-party phrases match six vendor pages, 6 of 6 (#43). A run on a stock Android 36 emulator found 4 of 5 native Settings paths; one not found, run exited 1 (#51). Release v0.5.0.
- 2026-11-08: Two sentences no source backs were dropped from the habit summaries and the web password text, web and native (#62). Release v0.5.0.
- 2026-11-08: Notes only: FOUND.md and LEARNINGS.md additions (#40). No app change.
- 2026-11-08: Menu paths in the device-check fix steps now match the screens on Chrome for Android and Android 16, and a script to check them was added (#88). The script's Android step does not pass yet and no log is committed. Release v0.4.0.
- 2026-11-08: Three long sentences in the habits summaries were split, web and native; punctuation only (#65). Release v0.4.0.
- 2026-11-08: CI now runs on the self-hosted runner (#96); the CI run at 698dc92 passed lint and build (run 42482618888). Release v0.4.0.

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
