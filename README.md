# tiny-chess-01 entry

A chess engine in at most 4 KB of Python: negamax alpha-beta with PVS, quiescence search, a transposition table, null-move pruning and LMR over a 0x88 board, with an incremental material + piece-square evaluation. main.py is the whole engine (an LZMA-packed build of the source, as the rules allow); it plays the make.fun gauntlet through the env at MAKEFUN_ENV_URL, searching to a fixed node budget.
