# Nexus

**A minute to learn, a lifetime to master.**

Nexus is a 2-player abstract strategy game about spatial control and connection. It utilizes simple mechanics—placement and sliding—to create profound strategic depth where a single move can dramatically reshape the entire board.

This repository contains a browser-based implementation of Nexus, allowing you to play against an AI opponent.

---

## ⚠️ Attribution, Copyright, and License

### Game Concept and Design (Copyright)

The game mechanics, rules, concept, and the name "Nexus" were invented by **betterfuture2030**.

**Copyright © 2025 Peter Lowes.**

The intellectual property of the game design is retained by the inventor. Acknowledgment of the original inventor is requested for any derivative works or implementations based on these mechanics.

### Code Implementation (License)

The source code (HTML, CSS, JavaScript) in this repository is provided under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## Game Rules

The objective is to be the first player to connect all 8 of their pieces into a single, **orthogonally** (horizontally or vertically) connected group.

### Phase 1: Placement

1. The 8x8 board begins empty.
2. Starting with White, players alternate placing one piece onto any empty square.
3. This continues until all 16 pieces (8 per player) are placed.

### Phase 2: Movement (The Slide Mechanic)

After placement, the Movement Phase begins. **Black moves first** in this phase.

Players take turns moving one piece using the **Slide** mechanic:
* A piece slides in a straight line (horizontally, vertically, or diagonally).
* The piece moves until it is stopped by the edge of the board OR another piece.
* The piece stops in the square immediately adjacent to the obstruction.
* There are no jumps or captures.

#### Movement Example
```svg
<svg width="250" height="250" viewBox="0 0 80 80" xmlns="[http://www.w3.org/2000/svg](http://www.w3.org/2000/svg)">
  <defs>
    <pattern id="readme-grid" width="20" height="20" patternUnits="userSpaceOnUse">
        <rect width="10" height="10" x="0" y="0" fill="#f0d9b5"/>
        <rect width="10" height="10" x="10" y="10" fill="#f0d9b5"/>
        <rect width="10" height="10" x="10" y="0" fill="#b58863"/>
        <rect width="10" height="10" x="0" y="10" fill="#b58863"/>
    </pattern>
  </defs>
  <rect width="80" height="80" fill="url(#readme-grid)"/>
  <g stroke="#333" stroke-width="0.5">
    <line x1="0" y1="0" x2="80" y2="0"/>
    <line x1="0" y1="80" x2="80" y2="80"/>
    <line x1="0" y1="0" x2="0" y2="80"/>
    <line x1="80" y1="0" x2="80" y2="80"/>
  </g>

  <rect x="30.5" y="0.5" width="9" height="9" fill="rgba(50, 205, 50, 0.4)" stroke="green" stroke-width="1"/> <rect x="30.5" y="70.5" width="9" height="9" fill="rgba(50, 205, 50, 0.4)" stroke="green" stroke-width="1"/> <rect x="0.5" y="30.5" width="9" height="9" fill="rgba(50, 205, 50, 0.4)" stroke="green" stroke-width="1"/> <rect x="50.5" y="30.5" width="9" height="9" fill="rgba(50, 205, 50, 0.4)" stroke="green" stroke-width="1"/> <rect x="0.5" y="0.5" width="9" height="9" fill="rgba(50, 205, 50, 0.4)" stroke="green" stroke-width="1"/> <rect x="60.5" y="60.5" width="9" height="9" fill="rgba(50, 205, 50, 0.4)" stroke="green" stroke-width="1"/> <rect x="10.5" y="50.5" width="9" height="9" fill="rgba(50, 205, 50, 0.4)" stroke="green" stroke-width="1"/> <rect x="50.5" y="10.5" width="9" height="9" fill="rgba(50, 205, 50, 0.4)" stroke="green" stroke-width="1"/> <circle cx="35" cy="35" r="4" fill="white" stroke="black" stroke-width="0.5"/>

  <circle cx="65" cy="35" r="4" fill="black" stroke="white" stroke-width="0.5"/>
  <circle cx="65" cy="15" r="4" fill="black" stroke="white" stroke-width="0.5"/>
  <circle cx="15" cy="55" r="4" fill="black" stroke="white" stroke-width="0.5"/>

</svg>
