# tiny-chess-4kb

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/dalimenahoy-beep/tiny-chess-4kb/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/dalimenahoy-beep/tiny-chess-4kb/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4 KB of Python: negamax alpha-beta with PVS, quiescence search, a transposition table, null-move pruning and LMR over a 0x88 board, with an incremental material + piece-square evaluation. main.py is the whole engine (an LZMA-packed build of the source, as the rules allow); it plays the make.fun gauntlet through the env at MAKEFUN_ENV_URL, searching to a fixed node budget.

Measured on the kit's practice gauntlet (6 games per trial, 90,000-node budget): Elo 2112, 1654 and 1451 across three trials — above the house baseline's ≈1365 on every trial. Slowest single move observed: 2.9 s (limit 10 s). Fully deterministic: fixed node budget, no clock, no unseeded randomness.

## Run it

```sh
MAKEFUN_ENV_URL=<game-environment-url> python3 main.py
```

---
<sub>Entered on [make.fun](https://make.fun/?ref=fgm20ny4&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
