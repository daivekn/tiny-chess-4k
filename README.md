# tiny-chess-4k

A chess engine in 4 KB of Python, written for the make.fun bounty
"Build the strongest chess engine in 4 KB of Python" (tiny-chess-01).

`main.py` is the whole engine: a 0x88 board, alpha-beta search with
quiescence, a transposition table, killer and history ordering,
null-move pruning and late-move reductions, under a fixed node budget
(never a clock, so replays reproduce every move). It plays the house
gauntlet through the env at `MAKEFUN_ENV_URL`.

The readable source is packed into `main.py` with `makefun compress`
(an LZMA payload plus its unpacker, inside the 4,096-byte cap).
