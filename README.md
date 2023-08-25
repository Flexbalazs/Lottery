The program will ask for the players' names first: if there are no more players, enter * for the player name.
After that, each player can guess three numbers between 1 and 30. The program should ensure that a player can only guess a number once, and the entered numbers should be between 1 and 30!
Next is the draw, where the computer selects three different numbers out of 30.
Following this, the program displays the drawn numbers in ascending order, then the names of each player, their guessed numbers (in the order they were entered), and the count of correct guesses. The players will be displayed in decreasing order based on the count of correct guesses.
Then the program will ask if we want to play again, and if yes, it restarts; otherwise, it finishes the program.

If we directly enter *, then it would jump to asking if we want to play again.

To store the names, guesses, and the count of correct guesses, we'll use our own class called "Ticket". It has a two-parameter constructor (String name, Set<Integer> guesses). Accordingly it has the data members as well. In addition to the above two parameters, there is an int data member named "correctGuessesCount" which will be set by the "evaluate()" method. This method takes the set of winning numbers as a parameter (Set<Integer> winningNumbers). 

The Ticket class is "foolproof," meaning it checks for all erroneous inputs. If the name is invalid (null, empty), it should default to "Player". Also, the Ticket class will verify that the "guesses" received as constructor parameters are not null, have the appropriate number of elements, and that they are within the specified range. For incorrect guesses, an empty Set would be set.

For sorting the "CorrectGuessComparator" is responsible.
Our main running class is "Lotto," which also monitors the entered numbers (between 1 and 30, no duplicates, etc.).
