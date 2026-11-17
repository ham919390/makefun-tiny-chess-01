# makefun-tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ham919390/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ham919390/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in a single `main.py` of 4,042 bytes. The file unpacks and
execs an LZMA-compressed engine (compression is allowed; payload and
unpacker together stay under the 4,096-byte cap).

The engine: 0x88 board, negamax with alpha-beta and PVS, a transposition
table with mate-score adjustment, quiescence search with check evasions,
check extensions, MVV-LVA ordering, and a tapered material + piece-square
evaluation. It searches to a fixed node budget (60,000 nodes per move,
never a clock), so replays reproduce its moves exactly.
