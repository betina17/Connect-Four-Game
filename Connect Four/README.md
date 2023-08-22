# Connect Four Implementation in Python

## Overview

This project is a Python-based implementation of the classic game "Connect Four". The game consists of a 6x7 grid where two players take turns to drop their respective symbols (1 for the human player and 2 for the computer) into the columns. Due to the game's gravity rule, the dropped piece will fall to the lowest available position within the chosen column. The objective is to be the first to form a horizontal, vertical, or diagonal line of four of one's own symbols.

## Features

1. **Object-Oriented Programming (OOP)**: The implementation uses object-oriented programming principles, making use of classes and objects to represent the game's components such as the board, the game logic, and the user interface.
2. **Layered Architecture**: The code is structured using a layered architecture, separating the domain (board representation), services (game logic), and user interface.
3. **Color-coded Visualization**: The game board is displayed with color-coded symbols for better visualization. The human player's moves are displayed in red, while the computer's moves are in yellow.
4. **Input Validation**: The program checks for valid input from the human player, ensuring that the chosen column is within the range (0-6) and that the column isn't already full.
5. **Computer Player Strategy**: The computer player uses a simple strategy to make its moves. It first checks if it can win in the next move, then checks if it needs to block the human player from winning, and if neither of those conditions is met, it makes a random move.
6. **Winning Condition Check**: The game checks for a winning condition after every move. It checks horizontally, vertically, and both diagonal directions.
7. **Full Board Check**: The game also checks if the board is full after every move to determine if the game is a tie.

## Algorithm for Computer Player

The computer player follows a specific order of operations when deciding where to place its symbol:

1. **Check for Winning Move**: The computer first checks if there's a move that would allow it to win the game. This is done by looking for a sequence of three consecutive symbols of its own in any direction (horizontal, vertical, or diagonal) and checking if the fourth position is available.
2. **Block Human Player**: If the computer can't win now, it checks if the human player is about to win in their next move. This is done as well by looking for a sequence of three consecutive symbols of 1 (the human player symbol) in any direction (horizontal, vertical, or diagonal) and checking if the fourth position is available to place its move there and block the human player from possibly forming a line of four of his symbols and win.
3. **Random Move**: If neither of the above conditions is met, the computer makes a random move, choosing a random column, while respecting the gravity rule of the game. 

## How to Play

1. The game starts by displaying an empty board.
2. The human player is prompted to choose a column (0-6) to place their symbol.
3. After the human player's move, the computer makes its move, and the updated board is displayed, along with a message informing the player about the column where the computer just moved.
4. The game continues until there's a winner or the board is full.

To start the game, simply run the main script.


