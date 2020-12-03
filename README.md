# FlashCards

## Abstract

In this command-line quiz, the user is prompted, selects an answer to each question in a series of questions, and given feedback based on their response.

This is the first solo project of Mod 2 of the Front-End program at Turing School. The project was designed by [Turing School Staff](https://frontend.turing.io/projects/flash-cards.html) and implemented by me, [Alice Ruppert](https://github.com/srslie).

My goals were to learn to write tests, implement a dynamic program without a front-end (using only the command line and module-exports), use a linter on my code, and follow a guide to create this functionality in the span of only a few days.

Special thanks to my mentor, [Scott Schipke](https://github.com/sschipke), and my partner for their technical and emotional support.

## Functionality

You're prompted for each question, given the opportunity to select an answer, and then given feedback. You're able to play through the entire deck of cards, and shown the percent you guessed correctly at the end of the round:

![flash cards example gif](https://media.giphy.com/media/CKQgfRGHQevgkJVted/giphy.gif)

## Setup & Install

To play, clone this repo to your machine, and ```cd``` into the directory.

Type in ```node index.js``` and the game will begin!

You will be prompted with a question and set of answers. Choose the number (type it in or use the arrow keys to move up and down, and hit enter) to pick your answer.

You'll be given feedback as to whether your answer was "correct!" or "incorrect!".

At the end of the game, you'll be shown your percentage of correct answers.

Hit control-c to quit the game.

## Support, Design Decisions & Future Iterations

For any technical issues, please contact [Alice](mailto:aliceruppert@gmail.com).

My testing suite does not include Game.js tests. While initially I wrote them and they were important in designing the Game class, especially in its instantiation of the new classes needed, all those classes separately had unit tests. Since the main Game method required user input when run, an integration test would be needed. There was no easy way to mock the user input in within the tests, so I ended up deleting the test file. If you poke around the commits you can see the ghost of the code that once lived, but I look forward to setting up future code in a way that would be more testable, or using tests that could accomplish more with this set up!

I did start working on trying to create a prompt which asks the user if they would like to restart the game or exit. My understanding of this [inquirer](https://www.npmjs.com/package/inquirer) which is used to set up the other prompts is somewhat limited, so I struggled to accomplish this, but my intent was to set up two options, one which reinstantiates a new Game, the other which exits out of the node running back into the terminal.

No future iterations are currently planned, but to make this more exciting, more cards could be added. There could be a way for users to upload their own questions and answers for studying or trivia purposes. There could be a way to record scores between plays or users. There could be a snazzier front-end display or online deployment.

For now though, enjoy the simple flashcards!
