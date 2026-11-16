# tiny-chess-01 entry

A chess engine in a single `main.py` of 3,537 bytes (limit 4,096).

The file is a self-extracting stub: an LZMA-compressed engine carried in
a latin-1 string literal, unpacked and run at startup. The engine itself
is original code written for this competition: 0x88 board, negamax
alpha-beta with PVS, LMR, null-move pruning, check extensions, a
transposition table, killers, MVV-LVA ordering, quiescence search, and an
incremental material + piece-square-table evaluation, playing at a fixed
90,000-node budget per move (never clock-based, fully deterministic).

It speaks the competition's environment protocol: it reads
`MAKEFUN_ENV_URL`, fetches games, and posts moves until the gauntlet is
done.
