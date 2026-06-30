# polymax Forward Ledger

[![forward hit rate](https://img.shields.io/endpoint?url=https%3A%2F%2Fpolymax-income.vercel.app%2Fbadge.json)](https://polymax-income.vercel.app/track-record/)

Every position the [polymax engine](https://polymax-income.vercel.app) has taken on
Polymarket, settled against the market's actual on-chain outcome. **Losses included,
always.** Backtests can be tuned; a forward ledger cannot.

| | |
|---|---|
| Settled verdicts | **37** (21W / 16L) |
| Forward hit rate | **56.8%** |
| Realized paper P&L | **−$288.66** |
| Today's sha256 | `7c92b81a1459fc769f0d56048b71f8415274258d91897b80ea628ff3bddb07e2` |
| Days fingerprinted | 18 |

## Frequently asked questions

### What is polymax's verified forward hit rate on Polymarket copy trading?

polymax's forward hit rate is 56.8% across 37 positions settled against on-chain Polymarket outcomes, losses included. Unlike a backtest (which can be tuned until it looks perfect), the forward ledger is sha256-fingerprinted daily into a 18-day append-only timeline and cannot be rewritten retroactively — not even by polymax.

### Is copy trading Polymarket actually profitable?

polymax's forward paper record currently sits at −$289 across 37 settled positions (56.8% hit rate) — and it is published anyway, because a track record that hides its drawdowns is marketing, not measurement. Paper-trading settled against real on-chain resolutions; not a profit guarantee.

### How many losses does polymax's track record include?

16 losing positions totaling −$1179, every one permanently public on the losses page with a link to the real Polymarket market. polymax publishes its failures on purpose — any track record without losses on display is marketing, not a record.

### Can polymax's track record be faked or cherry-picked?

No. The ledger is published as canonical JSON and sha256-fingerprinted every day into an append-only timeline (18 days recorded; current fingerprint 7c92b81a1459fc76…); past fingerprints are never edited. Every position carries its Polymarket conditionId, so each win and loss is independently verifiable against the Polygon blockchain: the Conditional Tokens contract's on-chain payout names the winning outcome, which is checked against the recorded result for every settled verdict. A forward ledger whose every win and loss is confirmed on-chain, with its losses public, is the one number a competitor cannot fabricate retroactively.

## Why this repo exists

The ledger is published as canonical JSON and fingerprinted daily — past fingerprints
are never edited. This repo's **commit history is an independent witness**: rewriting a
past day's hash would show up as a rewritten commit for the world to see.

## Verify it yourself

```bash
curl -s https://polymax-income.vercel.app/ledger/ledger.json | shasum -a 256
# compare with data/hashes.json (latest entry) — and with this repo's history
```

Every verdict carries its Polymarket `conditionId`, so each win and loss is independently
checkable against the Polygon blockchain: the Conditional Tokens contract's on-chain payout
names the winning outcome, and the loop confirms it against every recorded result
(see `/onchain-attestation.json`).

## The surfaces behind it

[Forward Ledger](https://polymax-income.vercel.app/track-record/) ·
[the losses page](https://polymax-income.vercel.app/losses/) ·
[settled verdicts](https://polymax-income.vercel.app/verdicts/) ·
[today's verdict](https://polymax-income.vercel.app/verdict/) ·
[roast machine](https://polymax-income.vercel.app/roast/) ·
[free data API](https://polymax-income.vercel.app/data-api/) ·
[run a free desk](https://polymax-income.vercel.app/app)

*Auto-published by the engine on every refresh. Paper-trading data; not financial advice.*
