# icec4
The Connect Four Game Project is a Python implementation of the classic Connect Four board game. Players take turns dropping their tokens (X or O) into a vertical grid, aiming to connect four tokens consecutively in a row, column, or diagonal. The project showcases fundamental programming concepts of connect four game.
The game starts by creating a 6x7 empty game board using the create_board() function.

The main() function initializes the current player as 'X'.

The game enters an infinite loop where the game board is displayed, and the current player is prompted to choose a column to drop their token.

The player enters their chosen column (0 to 6), and the input is stored in the col variable.

The game checks whether the entered column is valid (between 0 and 6). If it's not valid, an error message is displayed, and the loop continues to the next iteration, prompting the same player to enter a valid column again.

If the entered column is valid, the drop_token() function is called with the current player's token ('X' or 'O') and the chosen column. The function tries to drop the token into the chosen column from the bottom of the column.

If the drop is successful (i.e., the column is not already full), the game checks for a win condition using the check_win() function:

a. The function first checks for horizontal wins by iterating through each row and checking if there are four consecutive tokens of the current player.

b. Then, it checks for vertical wins by iterating through each column and checking if there are four consecutive tokens of the current player.

c. Next, it checks for diagonal wins from bottom-left to top-right by iterating through the rows and columns and looking for four consecutive tokens.

d. Finally, it checks for diagonal wins from top-left to bottom-right.

If a win condition is met, the game board is printed, and a message is displayed indicating that the current player has won. The loop breaks, and the game ends.

If there is no win, the game checks for a draw condition. This is done by checking if all columns in the top row are filled. If so, the game board is printed, and a message is displayed indicating that the game is a draw. The loop breaks, and the game ends.

If neither a win nor a draw condition is met, the game switches the current player's turn. If the current player is 'X', it becomes 'O', and vice versa.

If the chosen column was full (i.e., the drop_token() function returned False), an error message is displayed, indicating that the player needs to choose another column.

The loop then continues to the next iteration, displaying the updated game board and prompting the new current player to choose a column.

This sequence of events repeats until a player wins, the game ends in a draw, or the players decide to exit the game. This creates the back-and-forth gameplay characteristic of Connect Four.
