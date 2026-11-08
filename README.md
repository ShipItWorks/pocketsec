# PocketSec

Find out how hackable you are in 60 seconds. The scan runs in your browser.

**Score: 63 / 100** on our own [rubric](https://shipitworks.com/how-we-score/). Stage: Beta. Scored 2026-11-01; this record was updated 2026-11-07 from the [product page](https://shipitworks.com/apps/#pocketsec).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Web (static site). Android wrapper planned; not on Google Play.

## What works today

- Shield Score + grade; demo = 66/C (CLAUDE.md claim)
- Static site builds and renders 3 routes
- Live site reachable

## Not done yet

- The UI, the device check (AUTO-1..5), the habits audit (HAB-1..6), the HIBP range call and the PDF report are all still untested and were not run
- No TWA or AAB; assetlinks.json still holds REPLACE_WITH_ placeholders; the Play 12x14 closed-test rule applies
- LICENSE.md is PolyForm Noncommercial while the plan says All rights reserved - mismatch unresolved
- No CSP header; contrast, keyboard and TalkBack not checked; dark theme is fixed with no light mode

## What changed

- 2026-11-07: The 39 native Android engine unit tests pass on a Linux JVM (logged; not run on a phone). The native README credits ShipItWorks and the public support address, a CHANGELOG was added, and the CI actions are pinned to commit SHAs. Release v0.3.0.

Full list with release tags: [CHANGELOG](CHANGELOG.md).

## Demo

[Transcript of the demo (1:20)](https://shipitworks.com/pocketsec/transcript/) · video on the [product page](https://shipitworks.com/apps/#pocketsec)

The demo voice is AI-generated (ElevenLabs, "Alice") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README and a CHANGELOG, and soon a LICENSE. Until the source is public, the [product page](https://shipitworks.com/apps/#pocketsec) is the source of truth, and the score above is the one to trust.

## How we work

Say only what we can back. Say what is not finished before anyone asks. Name people, companies and tools to give credit. Collect as little data as possible. We use AI and say so: Claude (by Anthropic) helps write the code and wrote this README.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02. Owner review by Robert Sweetman: pending.
