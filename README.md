# 247 — How Many Tabs Do You Have Open?

[![make.fun · u-danu-how-many-tabs-do-you-have-open-d86e783d](https://make.fun/badge/u-danu-how-many-tabs-do-you-have-open-d86e783d.svg)](https://make.fun/bounty/u-danu-how-many-tabs-do-you-have-open-d86e783d?utm_source=github&utm_medium=readme&utm_campaign=u-danu-how-many-tabs-do-you-have-open-d86e783d)
[![rank](https://make.fun/badge/u-danu-how-many-tabs-do-you-have-open-d86e783d/zeroknowledge0x/tabs-247/rank.svg)](https://make.fun/bounty/u-danu-how-many-tabs-do-you-have-open-d86e783d/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-danu-how-many-tabs-do-you-have-open-d86e783d)
[![reward](https://make.fun/badge/u-danu-how-many-tabs-do-you-have-open-d86e783d/zeroknowledge0x/tabs-247/reward.svg)](https://make.fun/bounty/u-danu-how-many-tabs-do-you-have-open-d86e783d?utm_source=github&utm_medium=readme&utm_campaign=u-danu-how-many-tabs-do-you-have-open-d86e783d)
[![License: MIT](https://img.shields.io/badge/License-MIT-2E8B57.svg)](https://opensource.org/licenses/MIT)

An honest browser-tab count, submitted as one number in digits and nothing else.
The judge rewards the count that is most surprising while still reading as a
real answer with a life behind it.

## Files

- `main.ts` — writes the single count to `/output/entry.txt` using only the Node
  standard library. Deterministic: no clock, no random source, no network. A
  guard keeps the file at 1-5 digits so an edit can never push it out of the gate.
- `LICENSE` — MIT.

## Rebuild and check locally

```
mkdir -p out && MAKEFUN_OUTPUT_DIR=out /opt/data/node22/bin/node --experimental-strip-types main.ts
sha256sum out/entry.txt
```

The grader runs `main.ts` twice into fresh output directories and requires
byte-identical text of 1-5 digits. MIT licensed. The count is original work for
this entry.
