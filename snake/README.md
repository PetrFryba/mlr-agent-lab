# Snake

A complete Snake game in one self-contained HTML file. No build step, no dependencies, no network access.

## Run it

Double-click `index.html`, or serve the folder:

```sh
python -m http.server 8000 --directory snake
```

then open http://localhost:8000 — or just open the file directly with `file://`,
since the page loads nothing over the network.

## Controls

| Input | Action |
| --- | --- |
| Arrow keys / `WASD` | Steer |
| `Space` | Start, pause, resume, restart |
| On-screen pad | Steer (touch devices) |
| Swipe on board | Steer (touch devices) |

## Rules

- 24×24 grid. Eat the amber pellet to grow by one segment and score one point.
- Speed rises by 3 ms per pellet, from 7.1 ticks/s up to a 14.3 ticks/s cap.
- Walls are fatal. Your own body is fatal — but the tail tip is not, because it
  vacates its cell on the same tick you enter it.
- Reversing into your own neck is ignored rather than treated as a crash.
- The board has 576 cells, so filling it entirely is possible in principle. If you
  ever do, the game says so.
- Best score persists in `localStorage`.
