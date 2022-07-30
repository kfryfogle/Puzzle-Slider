# Puzzle-Slider

Updated Final Project for CS 5001: Intensive Foundations of Computer Science at Northeastern University.

For this project, I wanted to utilize the practices I learned in my Object Oriented Design course to update a project I did in my Foundations of CS course which I took in the Fall.
In the original project, I utilized procedural methods in order to carry out this task.
In this new version, object oriented practices allowed me to drastically reduce the amount of code I produced procedurally and made my project much more uniform in the process.

I utilized a main class called game that withheld three class objects as attributes. These three objects were utilized to prioritize and manage their own respective aspects of the board: the Scoreboard, Leaderboard, and Popup objects in the game. The Scoreboard object was in charge of updating the scoreboard with each click, as well as withholding information such as the current total moves, and max moves. The Leaderboard object was used to check if the user got within the top 5 high scores and to update the leaderboard if the user has done so. The Popup object was used to manage visibility of popup messages if the game was won, lost or quit by the user.

Since the Game class withholds the information for the current game being played, it also holds all 16 game Tiles within a list. The tile class made it much easier to keep track of each tiles turtle object. This list made it much easier to keep track of all the tiles, as the blank tile was always in index 0. The Game class always kept track of the current position of the blank tile, much like the Position Service class in versions prior.

Within the game class, I decided to update the click method in prior versions to game_click. This new click method was done more dynamically than the first version, as it looks for the 4 legal click locations around the white tile where it checks if each tile is visible in order to switch with them. This is a much cleaner way of writing the method as originally it was written for each specific case, for each individual game.

Overall, this rework allowed me to make one singular game class rather than 3 individual game methods. To add onto this, there are new methods for file checking and creation. This means if leaderboard directories and files are missing, the game will create a new document or file based off what information is missing. Also, the outline method has been cleaned up slightly as well in order to create cleaner code. Overall, this version runs much faster and has less bugs than the original.
