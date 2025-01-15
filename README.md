The provided code is a Java program for a simple game called "Guess the Number." In this game, the program generates a random number between 1 and 100, and the user tries to guess it. After each guess, the program gives feedback, and the game continues until the user guesses the number correctly. Here's an elaborate explanation of how the code works:


---

1. Random Number Generation

Random rand = new Random();
int numberToGuess = rand.nextInt(100) + 1;

A Random object is created to generate a random number.

rand.nextInt(100) generates a random integer between 0 (inclusive) and 100 (exclusive). Adding 1 shifts the range to 1–100.



---

2. Game Variables

int attempts = 0;
int score = 0;
Scanner scanner = new Scanner(System.in);

attempts: Keeps track of how many guesses the user has made.

score: Calculates the score based on the number of attempts.

scanner: A Scanner object is used to read user input from the console.



---

3. Main Game Loop

The game runs in an infinite while (true) loop until the user correctly guesses the number.


---

3.1. User Input

System.out.println("Enter your guess (1-100):");
int userGuess = scanner.nextInt();

The program prompts the user to enter their guess.

The user's guess is read and stored in the userGuess variable.



---

3.2. Increment Attempts

attempts++;

Each time the user makes a guess, the attempts counter increments by 1.



---

3.3. Correct Guess

if (userGuess == numberToGuess) {
    score = 100 - (attempts - 1) * 5;
    System.out.println("Congratulations! You found the number in " + attempts + " attempts.");
    System.out.println("Your score is " + score);
    break;
}

If the user guesses the correct number, the program calculates their score:

The base score is 100.

Each incorrect attempt deducts 5 points.


The program congratulates the user and displays their attempts and score.

The break statement exits the loop, ending the game.



---

3.4. Incorrect Guess

else if (userGuess < numberToGuess) {
    System.out.println("Too low! Try again.");
} else {
    System.out.println("Too high! Try again.");
}

If the user's guess is too low or too high, the program provides a hint.



---

4. Exit the Game

scanner.close();

The program closes the Scanner object to release resources.



---

Features

1. Random Number: Ensures replayability as the number changes each time.


2. Feedback: Provides hints for the user's next guess.


3. Score System: Encourages fewer attempts with a scoring mechanism.


4. User-Friendly: Simple prompts and clear messages for an enjoyable experience.




---

How to Play

1. Run the program.


2. Enter guesses between 1 and 100.


3. Follow the hints to adjust your next guesses.


4. When you guess the correct number, the program shows the number of attempts and your final score.




---

Example Run

Enter your guess (1-100):
50
Too low! Try again.
Enter your guess (1-100):
75
Too high! Try again.
Enter your guess (1-100):
63
Congratulations! You found the number in 3 attempts.
Your score is 90

This simple yet engaging program is a great example of basic control structures (loops, conditions), random number generation, and user input handling in Java.

