# Simple OpenGL Tic-Tac-Toe

A classic Tic-Tac-Toe game built with Python and the PyOpenGL library. This project serves as a clear and straightforward example of how to create a simple, interactive 2D game using basic OpenGL primitives and GLUT for window management.

---

## Features

- **Graphical Interface:** A clean, minimalist game window rendered with OpenGL.
- **Interactive Gameplay:** Full mouse support for placing X's and O's on the board.
- **Two-Player Mode:** Supports a classic hot-seat two-player game.
- **Win/Draw Detection:** Automatically detects and announces if a player has won or if the game is a draw.
- **Restart Functionality:** A simple "Restart" button to quickly start a new game.
- **Responsive Window:** The game board and UI elements correctly resize when the window is adjusted.

---

## Requirements

To run this game, you will need to have Python 3 installed, along with a few specific libraries.

- **Python 3.x**
- **PyOpenGL:** The main library for OpenGL bindings in Python.
- **PyOpenGL-accelerate:** An optional but highly recommended package that improves the performance of PyOpenGL.
- **GLUT (or freeglut):** A window system utility library. This is a system dependency and is **not** installed via pip.

---

## Installation

Follow these steps to set up your environment and run the game.

### 1. Install System Dependencies (GLUT)

GLUT is required for PyOpenGL to create a window. The installation process depends on your operating system.

#### On Debian/Ubuntu Linux:
```bash
sudo apt-get update
sudo apt-get install python3-opengl freeglut3-dev

#### On macOS (using Homebrew):

```bash
brew install freeglut
```

#### On Windows:

GLUT is often included with graphics drivers. If not, you can download pre-compiled GLUT binaries.
A simple way is to download `glut-3.7.6-bin.zip` from an unofficial source and place `glut32.dll` (or `freeglut.dll`) in the same directory as the `tictactoe.py` script, or in your system's `System32` folder.

---

### 2. Install Python Libraries

Once GLUT is available on your system, install the required Python packages using pip:

```bash
pip install PyOpenGL PyOpenGL-accelerate
```

---

### 3. Run the Game

With all dependencies installed, you can run the game directly from your terminal:

```bash
python tictactoe.py
```

A window should appear, and you can start playing!

---

## How to Play

1. Run the script as described above.
2. The game starts with Player X's turn.
3. Click on any empty cell on the grid to place your piece.
4. Turns will automatically alternate between Player X and Player O.
5. A message at the bottom of the window will announce the winner or declare a draw.
6. Click the "Restart" button at any time to clear the board and start a new game.

---

## Code Overview

The script is structured into several key sections:

* **Imports and Constants**
  Sets up the necessary libraries and defines global constants for colors, player types, and window dimensions. This makes the code easy to read and modify.

* **Game State Variables**
  A set of global variables (`board`, `currentPlayer`, `gameOver`, etc.) that track the current state of the game.

* **Drawing Functions (`draw_*`)**
  A collection of functions responsible for rendering different elements on the screen, such as the grid, the X's and O's, text, and the restart button.

* **Game Logic (`check_win`, `check_draw`, `reset_game`)**
  These functions contain the rules of Tic-Tac-Toe. They determine if a move results in a win or a draw and handle the game reset logic.

* **OpenGL Callbacks (`display`, `reshape`, `mouse_click`)**
  These are the core event-driven functions that GLUT calls in response to system events like needing to redraw the screen, resizing the window, or a mouse click.

* **Main Function (`main`)**
  The entry point of the application. It initializes GLUT, creates the game window, registers all the callback functions, and starts the main event loop.

---

Enjoy the game!

```
