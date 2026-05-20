# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the project

Open `index.html` directly in a browser — no build step, server, or dependencies required.

## Architecture

The entire application lives in `index.html` as a single self-contained file:

- **Styles** — inline `<style>` block; dark theme using a navy/red/teal palette
- **Markup** — static 3×3 grid of `.cell` divs, a score bar, a status line, and a Restart button
- **Logic** — inline `<script>` block; all game state (`board`, `current`, `gameOver`, `scores`) is held in plain JS variables with no external libraries

Game flow: click handler on each cell → updates `board[]` → `checkWinner()` scans the 8 win patterns → updates status/score display or toggles the current player.
