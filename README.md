# Minesweeper in C++ 💣

![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Algorithm](https://img.shields.io/badge/Algorithm-Flood_Fill-red?style=for-the-badge)
![Console](https://img.shields.io/badge/Platform-Console-black?style=for-the-badge)

## 📖 Overview

A terminal-based implementation of the classic **Minesweeper** puzzle. It features a grid-based gameplay loop where the player must uncover cells without detonating hidden mines.

## 💻 Technical Implementation

### Core Algorithms
1.  **Grid Initialization**:
    -   The game board is represented as a 2D array (matrix).
    -   **Mine Placement**: Uses `rand()` seeded with `srand(time(0))` to stochastically distribute mines across the coordinates, ensuring a unique board every session.

2.  **Flood Fill (Recursive Reveal)**:
    -   When a user selects a "blank" cell (value 0), a recursive function triggers to automatically reveal all adjacent blank cells.
    -   **Base Case**: The cell is a mine or has a non-zero number.
    -   **Recursive Step**: Iterate through all 8 neighbors (N, S, E, W, NE, NW, SE, SW) and call the reveal function.

3.  **Proximity Calculation**:
    -   During setup, the code iterates through every non-mine cell to calculate its number value by checking the 8 surrounding cells for the presence of mines.

## 🕹️ Control Logic

The game loop continues until:
-   **Win Condition**: All non-mine cells are revealed.
-   **Loss Condition**: A coordinates containing a mine is selected.

Input is handled via standard `cin` streams, accepting row and column integers.

## 📂 Source Code

-   **`minesweeps1.cpp`**: The primary implementation with standard difficulty.
-   **`minesweeps2.cpp`**: A variation with potentially different grid sizes or mine density.

## 🚀 How to Play

1.  Compile:
    ```bash
    g++ minesweeps1.cpp -o minesweeper
    ```
2.  Run:
    ```bash
    ./minesweeper
    ```

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## 👤 Author

**Simran Agarwal**
-   [Profile](https://github.com/officialsimranagarwal)
-   [LinkedIn](https://linkedin.com/in/simran-agarwal-54751b191)

---
*Generated with ❤️ by Simran Agarwal*
