# polymax Forward Ledger

[![forward hit rate](https://img.shields.io/endpoint?url=https%3A%2F%2Fpolymax-income.vercel.app%2Fbadge.json)](https://polymax-income.vercel.app/track-record/)

Every position the [polymax engine](https://polymax-income.vercel.app) has taken on
Polymarket, settled against the market's actual on-chain outcome. **Losses included,
always.** Backtests can be tuned; a forward ledger cannot.

| | |
|---|---|
| Settled verdicts | **4** (2W / 2L) |
| Forward hit rate | **50.0%** |
| Realized paper P&L | **−$71.49** |
| Today's sha256 | `77bd238852e2e9bcf41638912f8bc85b02f457f6bf862275553632e15efee8aa` |
| Days fingerprinted | 1 |

## Why this repo exists

The ledger is published as canonical JSON and fingerprinted daily — past fingerprints
are never edited. This repo's **commit history is an independent witness**: rewriting a
past day's hash would show up as a rewritten commit for the world to see.

## Verify it yourself

```bash
curl -s https://polymax-income.vercel.app/ledger/ledger.json | shasum -a 256
# compare with data/hashes.json (latest entry) — and with this repo's history
```

Every verdict carries its Polymarket `conditionId`, so each outcome is independently
checkable on-chain.

## The surfaces behind it

[Forward Ledger](https://polymax-income.vercel.app/track-record/) ·
[the losses page](https://polymax-income.vercel.app/losses/) ·
[settled verdicts](https://polymax-income.vercel.app/verdicts/) ·
[today's verdict](https://polymax-income.vercel.app/verdict/) ·
[roast machine](https://polymax-income.vercel.app/roast/) ·
[free data API](https://polymax-income.vercel.app/data-api/) ·
[run a free desk](https://polymax-income.vercel.app/app)

*Auto-published by the engine on every refresh. Paper-trading data; not financial advice.*
