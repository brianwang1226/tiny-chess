[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/brianwang1226/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/brianwang1226/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# tiny-chess

A chess engine in under 4 KB of Python, built for make.fun's tiny-chess-01.
It plays the gauntlet through the env at `MAKEFUN_ENV_URL`.

- 0x88 board, alpha-beta negamax with quiescence (captures and promotions)
- Move ordering by MVV-LVA, iterative deepening to a fixed node budget
- Material plus centralisation and pawn-push evaluation, bishop-pair bonus
- Deterministic: fixed node budget, never a clock, no unseeded randomness

`main.py` is the entrypoint, packed from the readable `engine.py` with the
kit's `makefun compress` (LZMA), so it fits the 4,096-byte cap. Python 3.13,
standard library only.
