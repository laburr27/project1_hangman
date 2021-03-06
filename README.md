Technologies Used: I used JavaScript (including jQuery), HTML, and CSS to build the Hangman game, along with Git and Github to load it online.  I used Atom as a text editor and iTerm to commit and push changes to the Git repository.

Approach Taken: I wanted to make the game playable by one person while not manually entering a list of words in an array, so I found the code for loading a web page- in this case, a text file which I pushed as part of the gh-pages branch- parsing it into individual lines, randomly selecting a line from the file (a word), and converting it to an array for the iterations needed to compare guesses to the answer.  I broke the program down into several functions to make it easier to debug if any issues arose.  The functions allow the game to register user input as a letter or a word and compare it to the array of letters in the answer and the answer in string form respectively, then recording the guess and printing it on the screen to the list of previous guesses.  If a word is guessed and is the answer, the game ends and the user is asked whether or not they want to play again.  If the user guesses a letter and it is on the board, a box covering the letter is removed for each occurrence in the answer.  If a guess is not the answer or included in it, a body part is added to the gallows and a prompt notifies the user that the guess was incorrect, along with the number of guesses left.

Installation Instructions: You can play the game at https://pretorben.github.io/project1_hangman/.

Unsolved Problems: The game functions properly, but there are some issues, primarily cosmetic.  The most glaring is the timing of prompts when winning the game.  While I was able to successfully use the setTimeout() function to rig the timing of alerts so they didn't fire before the CSS and HTML elements were set, setTimeout didn't work with my prompt asking if the user would like to play again.  The prompt window would appear, but even a 'yes' response caused the game to end.  I was unable to determine why this was happening, so I took out any setTimeout functions that would have fired should a user win the game; because of this, not all of the covering boxes will disappear if the user guesses the word prior to guessing all of the letters.

User Stories:
1. As a user, I should be able to play the game multiple times without having to refresh the page.
2. As a user, I should have previous guesses shown to me as a reference.
3. As a user, I should be able to see both a graphical and numerical representation of how many misses I have left.
4. As a user, I should be able to guess the word if I know it rather than having to fill in all the blanks.
5. As a user, I should be able to play this game on various devices- desktop, cell phone, tablet, etc.
