# ❌⭕ Tic Tac Toe (Python CLI)

A command-line implementation of the classic Tic Tac Toe game. This project uses Python to manage game state, handle user inputs, and determine the winner using a custom logic algorithm.

## 📋 Features
* **Two-State Tracking:** Uses separate lists (`xState` and `zState`) to track moves for Player X and Player 0 independently.
* **Custom Win Logic:** Determines the winner by summing the values of winning combinations.
* **Dynamic Board Rendering:** Updates the console display in real-time after every move.
* **Turn Toggling:** Automatically switches between Player X (1) and Player 0 (0).

## 🛠️ Implementation Logic (How it works)
This code was built using the following logical steps:

1.  **State Management:**
    * The board is represented by 9 positions (0-8).
    * Two lists, `xState` and `zState`, are initialized with zeros. When a player moves, the value at that specific index changes from `0` to `1`.

2.  **Board Visualization (`printBoard`):**
    * The function checks every position (0-8).
    * It uses **ternary operators** to decide what to print:
        * If `xState[i]` is 1 → Print `'X'`
        * If `zState[i]` is 1 → Print `'0'`
        * Else → Print the position number (e.g., `3`) so users know what to type.

3.  **Winning Algorithm (`checkWin`):**
    * All possible winning triplets (rows, columns, diagonals) are stored in a list: `[[0,1,2], [3,4,5], ...]`.
    * The code iterates through these triplets and uses a custom `sum()` function.
    * **Logic:** If `xState[a] + xState[b] + xState[c] == 3`, it means X has occupied all three spots in that line, so X wins.

4.  **The Game Loop:**
    * A `while(True)` loop keeps the game running.
    * It takes integer input from the user to update the state lists.
    * The turn variable toggles using the logic: `turn = 1 - turn`.

## 🚀 Getting Started

### Prerequisites
* Python 3.x installed on your system.

### How to Run
1.  **Clone this repository:**
    ```bash
    git clone [https://github.com/Rakshit842/Tic-tac-toe_python.git](https://github.com/Rakshit842/Tic-tac-toe_python.git)
    ```
2.  **Navigate to the folder:**
    ```bash
    cd Tic-tac-toe_python
    ```
3.  **Run the script:**
    ```bash
    python main.py
    ```
    *(Note: Replace `main.py` with the name of your python file if it is different)*

## 🎮 How to Play
1.  The board positions are numbered **0 through 8**.
2.  When asked "Please enter a value," type the number corresponding to the spot you want.
3.  **X** goes first.
4.  The game ends when a player completes a row, column, or diagonal.

## 📂 Code Structure
* `sum(a, b, c)`: Helper function to calculate the total of three board positions.
* `printBoard(xState, zState)`: Handles the visual representation of the grid.
* `checkWin(xState, zState)`: Validates if a winning condition is met.
* `main`: The entry point that handles the `while` loop and user input.

## 👤 Author
**Rakshit**
* **Course:** BCA (AI & DS) at K.R. Mangalam University
* **Focus:** Python Programming & Problem Solving
* **GitHub:** [@Rakshit842](https://github.com/Rakshit842)
* Connect with me on [LinkedIn](www.linkedin.com/in/rakshit-kamboj-326465318)

---
*This project was created as part of my 1st-year programming coursework.*
