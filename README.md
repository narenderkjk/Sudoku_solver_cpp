# 🎮 Sudoku CLI (C++/Windows)

A console-based Sudoku game written in modern C++ with 5 difficulty levels, an internal backtracking solver for validation and hints, a mistake tracking system, and color-coded board rendering using Windows console APIs.

## Features

- 5 difficulty levels: Easy, Medium, Hard, Expert, Evil
- Recursive backtracking solver with row/column/box pruning (powers validation and solution reveal)
- Hint system: show possible candidates for a cell
- Mistake tracking: up to 4 mistakes before Game Over
- Color-coded board rendering using Windows console attributes
- Interactive commands: `help`, `hint`, `focus`, `quit`, and direct move entry

## How It Works

- The game loads a predefined puzzle by difficulty, shuffles rows/columns within bands/stacks, and computes the full solution internally using recursive backtracking with pruning checks.
- Validation of user moves compares against the computed solution; hints enumerate valid candidates using row/column/box constraints.
- Color output uses Windows console attributes for readability (pre-filled, user entries, and highlights are distinguished by color).

## Requirements

- Windows OS (uses Windows APIs for console color)
- C++17-compatible compiler
  - MSVC (Visual Studio / Build Tools)
  - MinGW-w64 (g++)
