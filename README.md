# Sudoku Solver (FLTK GUI)

This is a C++ GUI-based Sudoku Solver built using the [FLTK](https://www.fltk.org/) (Fast Light Toolkit) library.  
It allows users to input a 9x9 Sudoku grid, validate the initial configuration, and solve it automatically using a backtracking algorithm.

---

## Features

- 9x9 interactive grid using `Fl_Int_Input` widgets  
- Validation of the initial Sudoku board before solving  
- Backtracking-based Sudoku solving algorithm  
- Clear button to reset the grid  
- Displays alerts for invalid or unsolvable boards  

---

## Algorithm Details
- Uses recursive backtracking to solve the board.
- Validates rows, columns, and 3x3 sub-grids before placing numbers.
- Backtracks when no valid number fits a cell.

---

## Requirements

- **C++17 (or later)**  
- **FLTK library (v1.3 or later)**  

---

## Installation

### 1. Install FLTK

#### Linux (Ubuntu/Debian):
```bash
sudo apt-get update
sudo apt-get install libfltk1.3-dev
```
#### MacOS (HomeBrew):
```bash
brew instsll fltk
```
#### Windows :
- Download the FLTK library from https://www.fltk.org/software.php
- Build and configure it in your compiler (e.g., MinGW or MSVC)

---

## Build Instructions

#### macOS (build as .app bundle):
```bash
g++ main.cpp -o main.app `fltk-config --cxxflags --ldflags`
open main.app
```
#### Windows (MinGW):
```bash
g++ main.cpp -o sudoku_solver -I<FLTK_INCLUDE_PATH> -L<FLTK_LIB_PATH> -lfltk
sudoku_solver.exe
```
