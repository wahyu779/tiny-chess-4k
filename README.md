# tiny-chess-4k

A chess engine in 4,031 bytes of Python, built for the
[make.fun tiny-chess-01](https://make.fun) competition: the strongest
engine in 4 KB of Python, rated against a fixed gauntlet of eight house
engines.

## How it plays

`main.py` is the whole engine. It talks to the competition env over HTTP,
plays each game in UCI, and searches with alpha-beta plus quiescence,
a transposition table, killer moves, and piece-square evaluation. The
search runs to a fixed node budget, never a clock, so replays play the
same moves.

Local practice trials (kit harness): mean Elo 1224 over 3 trials
(1173 / 1326 / 1173), above the 1154 practice floor.

## The size rule

- `main.py`: 4,031 bytes, at most 4,096. Standard library only; it
  reads, imports or runs no other file in this repository.
- Whole repository: under 8,192 bytes, no file over 4,096.

## License

MIT — see `LICENSE`.
