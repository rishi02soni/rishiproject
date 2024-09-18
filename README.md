# rishiproject
This is my first Git Repository . 
Just a Java game.....
import java.util.Scanner;
import java.util.Random;

public class GuessTheNumberGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        
        int randomNumber = random.nextInt(100) + 1; // Random number between 1 and 100
        int numberOfGuesses = 0;
        int guess = 0;

        System.out.println("Welcome to the Guess the Number Game!");
        System.out.println("I have chosen a number between 1 and 100. Try to guess it!");

        while (guess != randomNumber) {
            System.out.print("Enter your guess: ");
            guess = scanner.nextInt();
            numberOfGuesses++;

            if (guess < randomNumber) {
                System.out.println("Too low! Try again.");
            } else if (guess > randomNumber) {
                System.out.println("Too high! Try again.");
            } else {
                System.out.println("Congratulations! You've guessed the correct number in " + numberOfGuesses + " tries.");
            }
        }
        scanner.close();
    }
}

