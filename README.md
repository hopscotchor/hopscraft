# hopscraft

Self-driven quant research playground.

## Build Ideas

1. Strategy Lab (recommended)
- Goal: backtest one strategy end-to-end and generate a report.
- Stack: Backtesting.py + pandas + matplotlib.
- Output: equity curve, max drawdown, Sharpe, and trade log.

2. Parameter Researcher
- Goal: replace guesswork with systematic parameter search.
- Stack: vectorbt.
- Output: parameter heatmaps and walk-forward comparison.

3. Engineering Migration
- Goal: migrate research code into an event-driven architecture.
- Stack: NautilusTrader.
- Output: behavior comparison between research and production-style runs.

## Suggested Repo Layout

```text
/Users/hops/hopscraft/data
/Users/hops/hopscraft/strategies
/Users/hops/hopscraft/backtests
/Users/hops/hopscraft/reports
/Users/hops/hopscraft/NautilusTrader
```

## Minimal Task Checklist (DIY)

1. Pick one instrument and timeframe.
2. Implement a simple SMA crossover in `/Users/hops/hopscraft/strategies`.
3. Run a baseline backtest and save metrics to `/Users/hops/hopscraft/reports/baseline.md`.
4. Add commissions and slippage.
5. Run a parameter sweep and compare against baseline.
6. Do a walk-forward check and record overfitting signs.

## Definition of Done

- One reproducible command exists for each backtest.
- Report includes return, max drawdown, Sharpe, trade count, and win rate.
- Add a short note: what failed, what to try next.
