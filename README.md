# Conway's Game of Life

An implementation of [Conway's Game of Life](https://en.wikipedia.org/wiki/Conway's_Game_of_Life) using [Wasm](https://webassembly.org) and [Rust](https://www.rust-lang.org/learn).

### Theory

- The universe of the Game of Life is an infinite, two-dimensional orthogonal grid of square cells, each of which is in one of two possible states, live or dead, (or populated and unpopulated, respectively). Every cell interacts with its eight neighbours, which are the cells that are horizontally, vertically, or diagonally adjacent. At each step in time, the following transitions occur:
```
=> Any live cell with fewer than two live neighbours dies, as if by underpopulation.
=> Any live cell with two or three live neighbours lives on to the next generation.
=> Any live cell with more than three live neighbours dies, as if by overpopulation.
=> Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.
```
- These rules, which compare the behavior of the automaton to real life, can be condensed into the following:
```
=> Any live cell with two or three live neighbours survives.
=> Any dead cell with three live neighbours becomes a live cell.
=> All other live cells die in the next generation. Similarly, all other dead cells stay dead.
```

### Run
```bash
(If you want to build your own wasm binary)
> wasm-pack build --dev
...
(In project directory)
> cd www
> npm install
> npm run start
```
- Go to [localhost:8080](http://localhost:8080/)
