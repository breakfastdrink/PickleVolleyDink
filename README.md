# PickleVolleyDink

A pickleball scorekeeper.

## Usage

- Open `index.html` in a browser (no build required).
- Click `+` to add points to either team when they score.
- Click `Lost Serve` when the serving team loses the rally (receiving team wins the point).
- Keyboard shortcuts:
  - `1` — add point to Team A
  - `2` — add point to Team B
  - `3` — lose serve
  - `Z` — undo last action
  - `R` — reset match

## Game Settings

- **Game Length:** Choose 7, 9, 11, or 15 points
- **Win Condition:**
  - **Win by 2:** Standard pickleball rules (must win by 2 points)
  - **Hard Limit:** Tournament / Community Centre rules (first to reach the target score wins)
- **Match Type:** Doubles or Singles
- **Team Names:** Customize team names (longer names will negatively affect the UI -.-)

## Doubles Serve Rotation

When set to **Doubles** mode, the app enforces the correct serving rules:

- **Initial serve:** The starting team gets only one serve opportunity (1st server only).
- **Normal side-outs:** Each team gets two serves per side-out:
  - 1st server serves first; if they lose the rally, the 2nd server on the same team serves.
  - If the 2nd server loses the rally, service passes to the other team's 1st server.
- Use the `Lost Serve` button to mark when a serve is lost (rally won by the other team).
- The current server is displayed prominently (e.g., "0-0-1 · Team A · 1st server").

## Features

- Configurable game length and win condition
- Doubles/singles toggle with correct serve rotation logic
- Current server display with server number indicator (doubles mode)
- Undo/history and `localStorage` persistence
- Full keyboard support for fast scoring
- Mobile-optimized layout with responsive controls

## Notes

- Assisted by AI (persistent documentation, translation of logic)
- This is a static app using Tailwind CSS and Alpine.js.
- The scoring (`+` button) is independent of serve management (`Lost Serve`).
- Non-serving teams cannot score by accident—their button always works, but the red flash provides visual feedback.
- Problems? Open an issue. Features? Request it, fork, contribute.
