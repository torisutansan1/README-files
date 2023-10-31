# Q-learning-Tic-Tac-Toe
Minimax algorithm for a Tic-Tac-Toe Game

## Basic usage
To play the Tic-Tac-Toe game, you must run the `tic-tac-toe.py` file on an IDE like VSCode.

To play the game, you or the AI start. You are Player 1 corresponding with the letter "X" and the AI is Player 2 corresponding with the letter "O". If you start, you must enter a row and column from 1 to 3. Otherwise, the row and column numbers are invalid and you need to type a new row and column number.

If the AI starts, you wait until the AI finishes its turn for you to make another turn. The game finishes when either you or the AI manages to have 3 X's or O's in a given column or row.

## Background
The implementation of the tic-tac-toe game I provide uses different techniques to increase AI efficiency and decrease the runtime. I utilize the minimax algorithm with memoization to create my AI algorithm.

To use memoization, I change the __init__ function to create an empty set.

Then, I change the my_play function to create a recursive call for the minimax function and algorithm. This allows me to create my board, using rows and columns to create a tic-tac-toe game for the user to play with an AI.

There are multiple comments in my program that indicate where I use several techniques to increase AI efficiency. 

If the winner is O, then the self.judge.is_winner function returns 1, -1 if X.

I utilize the variables bestScore and bestMove for the miniMax algorithm. The Minimax algorithm I provide is a nested loop.

My original AI algorithm using the Minimax algorithm was inefficient, resulting in the usage of alpha and beta pruning. Using alpha-beta pruning, my algorithm is significantly more efficient.

The algorithm also utilizes a recursive call and my usage of memoization intends to decrease the runtime. The maximizing boolean variable allows the board to fill a slot with either O or X. bestScore stores currScore if currScore is greater than bestScore.

## Discussion
After 200,000 training games against itself with `epsilon=0.9`, the `QPlayer` seems practically unbeatable by a human player. It would be instructive, however, to check this by pitting it against a player following the [minimax](https://en.wikipedia.org/wiki/Minimax) algorithm for many games. It would also be interesting to check the finding by [Boyan (1992)](http://www.cs.cmu.edu/~jab/cv/pubs/boyan.backgammon-thesis.pdf) that a Q-learned player is able to beat the "T-hand" player 58% of the time and draw the remaining 42%.
