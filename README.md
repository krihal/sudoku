# Sudoku

A minimal, dependency-free Sudoku game in a single `index.html`. Works with keyboard only and on mobile phones.

## Features

- Six difficulties: Easy, Medium, Hard, Expert, Evil, Nightmare. Generated puzzles always have a unique solution and are graded by a built-in logic solver:
  - Easy / Medium: singles only (Medium has fewer clues)
  - Hard: needs naked pairs or pointing/claiming
  - Expert: needs naked triples, hidden pairs or X-Wing
  - Evil: needs XY-Wing, XYZ-Wing or Swordfish
  - Nightmare: beyond all of the above (chains, forcing, or trial and error)
- Two check modes (toggle with `C`):
  - **Instant check**: wrong numbers are flagged red as you place them
  - **Check at end**: nothing is flagged until the grid is full
- Fully keyboard-driven
- Touch-friendly on-screen number pad with remaining-digit counts
- Undo / redo, hints, timer
- Autosave in `localStorage`; resumes after refresh
- Light and dark theme (follows system)

## Keyboard

| Key | Action |
| --- | --- |
| Arrows / `WASD` / `HJKL` | Move selection |
| `1`-`9` | Place number |
| `0` / `Backspace` / `Delete` / `Space` | Erase cell |
| `Ctrl+Z` / `Ctrl+Y` (or `U` / `R`) | Undo / redo |
| `?` / `Shift+H` | Hint |
| `C` | Toggle instant check |
| `Shift+D` | Cycle difficulty |
| `N` | New game (press twice if a game is in progress) |

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy

Static file, no build step. On GitHub Pages: Settings → Pages → Deploy from branch → `main` / `/ (root)`.

## License

MIT, see [LICENSE](LICENSE).
