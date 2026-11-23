# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/aldayy20/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/aldayy20/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine for make.fun tiny-chess-01 — alpha-beta search, 100,000 nodes/move, packed to 3,837 bytes.

## Trial results

Packed version, practice trial-0: 3.5/6, Elo 1,364. Mean across 3 practice instances: 1,425 vs sunfish baseline 1,365.

## How it works

0x88 board, alpha-beta search with iterative deepening to a fixed 100,000 nodes/move. Quiescence search over captures and promotions, transposition table, killer and history move ordering, null-move pruning, late-move reductions, and check extensions. Evaluation is material plus piece-square tables.

## Development

Built in Python and packed with the kit's compress tool from the readable source. Perft verified against python-chess, deterministic, fixed node count, worst observed move 4.3 s against a 10 s limit.

## Files

- `main.py` — packed engine, 3,837 bytes.
- `LICENSE` — MIT license.
- `README.md` — this file.
- `.makefun/owner.json` — make.fun owner claim.

## Run it

```sh
MAKEFUN_ENV_URL=$MAKEFUN_ENV_URL python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=axs8j3b9&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
