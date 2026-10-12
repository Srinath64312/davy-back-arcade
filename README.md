# ⚡ Grand Line Arcade (`grand-line-arcade`)

> A versatile, offline multi-game gaming hub & Python zero-loop showcase featuring **Loopless Tic-Tac-Toe**, **Sudoku**, **Ludo Royale Mini**, **Gravity Drop-Toe**, and **Dots & Boxes Chaos**.

---

## 🎮 The Master Game Suite (`index.html`)

An ultra-sleek, zero-dependency offline web arcade playable anywhere:

1. **⚔️ Loopless Tic-Tac-Toe**:
   - Multi-Level AI: Easy (Buggy), Medium (Crocodile), Hard (Kizaru), and Pirate King (unbeatable Minimax AI).
   - Local PvP 2-player battles.
   - 100% loop-free architecture with AST test suite.
2. **🧩 Grand Line Sudoku**:
   - 4 Tiers: East Blue (Easy), Grand Line (Medium), New World (Hard), and Pirate King (Expert).
   - Pencil notes mode, auto-notes generator, Log Pose smart hints, timer, and mistakes counter.
3. **🎲 Ludo Royale Mini**:
   - Fast-paced 2-player arcade edition (Luffy Red vs. Zoro Green).
   - Animated 3D dice roll (roll 6 to deploy from base and earn bonus rolls).
   - Capture mechanics and Star (★) safe zones.
4. **🌪️ Gravity Drop-Toe**:
   - 3×3 board physics where pieces drop downward.
   - Players can choose to place a mark OR rotate the entire board 90° to trigger cascades!
5. **⚡ Dots & Boxes Chaos**:
   - Classic territory-capturing puzzle with dynamic line clicks, extra turns for boxes completed, and score trackers.

### 🌟 Shared Arcade Features:
- **Shared Pirate Bounty Ladder**: Climb from ฿30,000,000 (Rookie) all the way to ฿5,564,800,000 (PIRATE KING) across any game!
- **4 Visual Themes**: One Piece (Grand Line), Watermelon Cyber, Cyber Arcade, and Neo-Brutalist Pop.
- **Synthesized Web Audio Engine**: Tactile sound effects, dice rolls, tile drops, and victory fanfares generated in real-time.
- **Zero External Dependencies**: Pure vanilla HTML5, CSS3, and ES6+ JavaScript.

---

## 🐍 Python Zero-Loop Showcase

Is it possible to write a complete Tic-Tac-Toe game in Python without using **any** `for` or `while` loops?

**Yes!** By utilizing **tail recursion**, **immutable state transitions**, **unrolled index operations**, and **functional decomposition**, all traditional iterative loops are eliminated:
- No `for` loops
- No `while` loops
- No comprehensions (`[x for x in ...]`)
- No generator expressions (`(x for x in ...)`)

Includes an **AST validator** that programmatically inspects the codebase to prove that zero loop nodes exist.

---

## Quick Start

### 1. Clone or Download the Repository

```bash
git clone https://github.com/your-username/loopless-tictactoe.git
cd loopless-tictactoe
```

### 2. Run the Application

#### Launch Interactive CLI Menu:
```bash
python main.py
```

#### Launch Desktop GUI:
```bash
python main.py --gui
```

#### Run the AST Loopless Audit:
```bash
python main.py --check
```

---

## Running Tests

Run the full automated test suite (including game logic and the AST zero-loop audit):

```bash
python -m unittest discover tests
```

---

## How It Works Under the Hood

| Traditional Imperative Approach | Loopless Functional Approach |
|---|---|
| `while not game_over:` | **Tail Recursion**: `play_game_step(board, turn + 1)` |
| `while True: input(...)` | **Retry Recursion**: `get_human_move(board)` |
| `for row in grid:` | **Unrolled Direct Indexing**: `b[0]`, `b[1]`, ..., `b[8]` |
| `[i for i in range(9) if b[i] == ' ']` | **Recursive Tuple Fold**: `get_available_moves(board, idx)` |
| `for move in moves: minimax(...)` | **Recursive Minimax Search**: `_evaluate_moves_recursive(...)` |

---

## Repository Structure

```
loopless-tictactoe/
+-- src/
|   +-- __init__.py
|   +-- engine.py       # 100% loop-free core logic & Minimax AI
|   +-- cli.py          # Loop-free terminal UI & recursive prompts
|   +-- gui.py          # Event-driven desktop GUI (Tkinter)
|   +-- validator.py    # Loop-free AST static code analyzer
+-- tests/
|   +-- __init__.py
|   +-- test_engine.py  # Unit tests for wins, draws, immutability, AI
|   +-- test_ast.py     # Static AST tests enforcing zero loop constructs
+-- .gitignore
+-- LICENSE             # MIT License
+-- pyproject.toml      # Packaging metadata
+-- README.md           # Documentation
+-- main.py             # Main entry point & CLI/GUI dispatcher
```

---

## License

This project is licensed under the MIT License.
