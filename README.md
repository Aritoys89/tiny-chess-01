# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Aritoys89/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Aritoys89/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in a single `main.py` of 3,462 bytes (limit 4,096),
entered in make.fun's tiny-chess-01 bounty.

The file is a self-extracting stub: an LZMA-compressed engine carried in
a string literal, unpacked and run at startup. The engine itself is
original code written for this competition: 0x88 board, negamax
alpha-beta with PVS, LMR, null-move pruning, check extensions, a
transposition table, killers, MVV-LVA ordering, quiescence search, and an
incremental material + piece-square-table evaluation, playing at a fixed
90,000-node budget per move (never clock-based, fully deterministic).
In local practice against the kit's gauntlet it scored Elo 1451.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8932 python3 main.py
```

The engine speaks the competition's environment protocol: it reads
`MAKEFUN_ENV_URL`, fetches games, and posts moves until the gauntlet is
done.

---

<sub>Entered on [make.fun](https://make.fun/?ref=k7c6ejze&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
