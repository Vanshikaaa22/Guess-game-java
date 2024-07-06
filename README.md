# Guess-game-java
import java.util.Scanner;

public class GuessingGame {

  public static void main(String[] args) {
    // Generate a random number between 1 and 100
    int randomNumber = (int) (Math.random() * 100) + 1;

    // Initialize Scanner for user input
    Scanner scanner = new Scanner(System.in);

    int guess;
    int numGuesses = 0;

    do {
      System.out.println("Enter your guess (1-100): ");
      guess = scanner.nextInt();
      numGuesses++;

      if (guess == randomNumber) {
        System.out.println("Congratulations! You guessed the number in " + numGuesses + " tries!");
      } else if (guess < randomNumber) {
        System.out.println("Your guess is too low. Try again.");
      } else {
        System.out.println("Your guess is too high. Try again.");
      }
    } while (guess != randomNumber);

    scanner.close(); // Close the Scanner object
  }
}
