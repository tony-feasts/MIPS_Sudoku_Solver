# MIPS Sudoku Solver

## Overview
This is a Sudoku solver implemented in MIPS assembly. It was developed as a project for the course *Fundamentals of Computer Systems*. Test cases and helper functions below line 115 were provided by the course staff.

## Sudoku Background
A 9x9 grid starts with some cells pre-filled with numbers. A solved Sudoku board contains numbers 1-9 appearing exactly once in each row, column, and 3x3 box. Every valid starting configuration has a unique solution.

## Algorithm
The algorithm traverses each cell on the board. If a cell's value is determined, that number is ruled out from the possible values in the corresponding row, column, and 3x3 box. This process is repeated until the board is fully solved.

## Data Representation
- **Board Layout**: The board is represented as 81 cells stored in memory in row-major order.
- **Cell Structure**: Each cell uses 10 bytes, with the cell's possible values stored as a null-terminated string.

## Significant Procedures
- **`num_candidates`**: Counts the number of possible values for a cell.
- **`rule_out_of_cell`**: Removes a number from a cell's possible values.
- **`count_solved_cells`**: Counts the number of cells that have only one possible value.
- **`solve_board`**: Repeatedly traverses the board until it is solved.

## Running Instructions
To run the program, use the SPIM simulator:
1. Ensure SPIM is installed on your machine: `$ brew install spim`.
2. Navigate to the directory containing `sudoku.s`.
3. Run the program with the following command: `$ spim sudoku.s`.
