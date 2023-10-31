# Introduction
Minimax algorithm for a Tic-Tac-Toe Game

## Instructions
To play the Tic-Tac-Toe game, you must run the `tic-tac-toe.py` file on an IDE like VSCode.

To play the game, you or the AI start. You are Player 1 corresponding with the letter "X" and the AI is Player 2 corresponding with the letter "O". If you start, you must enter a row and column from 1 to 3. Otherwise, the row and column numbers are invalid and you need to type a new row and column number.

If the AI starts, you wait until the AI finishes its turn for you to make another turn. The game finishes when either you or the AI manages to have 3 X's or O's in a given column or row.

## Code Structure
The implementation of the tic-tac-toe game I provide uses different techniques to increase AI efficiency and decrease the runtime. I utilize the minimax algorithm with memoization to create my AI algorithm.

To use memoization, I change the __init__ function to create an empty set.
Storing these results in cache, to retrieve the same information allows the program to not need to compute known subproblems or information.

Then, I change the my_play function to create a recursive call for the minimax function and algorithm. This allows me to create my board, using rows and columns to create a tic-tac-toe game for the user to play with an AI.

There are multiple comments in my program that indicate where I use several techniques to increase AI efficiency. 

If the winner is O, then the self.judge.is_winner function returns 1, -1 if X.

I utilize the variables bestScore and bestMove for the Minimax algorithm. The Minimax algorithm I provide is a nested loop.

Algorithm Description:
My original AI algorithm using the Minimax algorithm was inefficient, resulting in the usage of alpha and beta pruning. Using alpha-beta pruning, my algorithm is significantly more efficient. In game theory, alpha-beta pruning allows me to cut off branches in the game tree that do not need to be searched. It knows a better move already exists. To add this optimization, I need to add alpha and beta as paramaters to the Minimax algorithm. Alpha corresponds to the maximizer and beta corresponds to the minimizer.

The algorithm also utilizes a recursive call and my usage of memoization intends to decrease the runtime. The maximizing boolean variable allows the board to fill a slot with either O or X. bestScore stores currScore if currScore is greater than bestScore.

## Background
Tic-tac-toe is a famous game where two players make move in a 3x3 board until one manages to get either an X or an O in an entire column or row. However, sometimes there is not another person to play with and the user wants to play with themselves. To solve this issue, a common tactic is to create an AI algorithm that creates a pseudorandom player.

## Conclusion
In conclusion, I find that game theory is particularly useful for 2d array games like tic-tac-toe. I did not know how to implement alpha-beta pruning prior to solving this problem and I think this project allows me to further understand its important. I am also happy to experiment with the Minimax algorithm to create an efficient 3x3 game of tic-tac-toe that the player can play with a bot.
