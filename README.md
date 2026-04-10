# 🧩 Sudoku Solver — Java

A console-based Sudoku solver implemented in **Java** using the **Backtracking algorithm**. It automatically solves any valid 9×9 Sudoku puzzle and prints the completed board to the terminal.

---

## 📌 Project Overview

This project demonstrates the classic **backtracking** approach to solving constraint satisfaction problems. Given a partially filled 9×9 Sudoku grid (with `0` representing empty cells), the program fills in all empty cells following standard Sudoku rules and prints the solved board.

---

## ✨ Features

- ✅ **Backtracking Algorithm** — Recursively tries digits 1–9 in each empty cell and backtracks if a conflict is found
- ✅ **Validity Checks** — Ensures no digit is repeated in the same row, column, or 3×3 sub-grid before placing it
- ✅ **Console Output** — Prints the solved board in a formatted grid with separators
- ✅ **Solution Detection** — Reports whether a solution exists or not

---

## 🧠 Algorithm Explained

The solver uses **recursive backtracking**:

1. Scan the board cell by cell (row by row, left to right)
2. If the current cell is already filled, move to the next cell
3. If the cell is empty, try placing digits `1` through `9`
4. For each digit, check if it is safe to place using `isSafe()`:
   - Not already in the same **row**
   - Not already in the same **column**
   - Not already in the same **3×3 box**
5. If safe, place the digit and recurse to the next cell
6. If recursion returns `false` (dead end), **backtrack** — reset the cell to `0` and try the next digit
7. If all 81 cells are filled successfully, return `true`

---

## 📋 Methods

| Method | Description |
|--------|-------------|
| `isSafe(sudoku, row, col, digit)` | Checks if placing `digit` at `[row][col]` is valid |
| `sudokuSolver(sudoku, row, col)` | Recursively solves the board using backtracking |
| `printSudoku(sudoku)` | Prints the solved 9×9 grid to the console |
| `main(String[] args)` | Defines the input puzzle and triggers the solver |

---

## 🔢 Sample Input Puzzle

The hardcoded puzzle used in `main()` (0 = empty cell):

```
0 0 8 | 0 0 0 | 0 0 0
4 9 0 | 1 5 7 | 0 0 2
0 0 3 | 0 0 4 | 1 9 0
------+-------+------
1 8 5 | 0 6 0 | 0 2 0
0 0 0 | 0 2 0 | 0 6 0
9 6 0 | 4 0 5 | 3 0 0
------+-------+------
0 3 0 | 0 7 2 | 0 0 4
0 4 9 | 0 3 0 | 0 5 7
8 2 7 | 0 0 9 | 0 1 3
```

---

## 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| Java | Core language for algorithm and console I/O |

---

## 📁 File Structure

```
Sudoku-Solver/
│
├── sudoku.java     # Main Java file with solver logic
└── README.md       # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
- Java Development Kit (JDK) installed — version 8 or above

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/SamruddhiNadgouda/Sudoku-Solver.git
   ```

2. **Navigate to the project folder**
   ```bash
   cd Sudoku-Solver
   ```

3. **Compile the Java file**
   ```bash
   javac sudoku.java
   ```

4. **Run the program**
   ```bash
   java sudoku
   ```

### Expected Output
```
Solution exists
-----------Sudoku Solver-----------
(solved 9x9 grid printed row by row)
```

---

## 🖼️ Output Preview

A screenshot of the terminal output is included in the repository.
![Screenshot 2024-03-28 124125](https://github.com/SamruddhiNadgouda/Sudoku-Solver/assets/97962486/2c3165d2-d117-4a4a-aac9-e803cd0dbae8)

---

## 🙋‍♀️ Author

**Samruddhi Nadgouda**   
GitHub: [@SamruddhiNadgouda](https://github.com/SamruddhiNadgouda)

