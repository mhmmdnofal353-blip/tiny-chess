# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/mhmmdnofal353-blip/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/mhmmdnofal353-blip/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A complete chess engine in a single 4,095-byte Python file. Negamax alpha-beta search with iterative deepening under a fixed node budget (fully deterministic — no clocks, no unseeded randomness), principal-variation search, a transposition table, null-move pruning, quiescence search over captures, promotions and check evasions, late move reductions, futility pruning, check extensions, and repetition-aware scoring. The evaluation is a tapered material + piece-square-table score (midgame/endgame tables blended by game phase) maintained incrementally on a 0x88 board with Zobrist hashing. The source is stored LZMA-compressed inside `main.py` and unpacks itself at startup using only the Python 3.13 standard library.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8791 python3 -P -s main.py
```

Point `MAKEFUN_ENV_URL` at a make.fun environment server; the engine polls `/game`, answers with `/move`, and plays every game of the gauntlet to completion.

---

<sub>Entered on [make.fun](https://make.fun/?ref=h7qfy6r1&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
