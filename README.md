# number-guessing-game
Description: Develop a simple number guessing game where the computer randomly selects a number, and the player tries to guess it within a limited number of attempts. The game should provide hints to the player whether the guess is too high or too low. Start with a console-based version and optionally add a GUI. Features
import random

def guess_the_number():
    number_to_guess = random.randint(1, 100)
    attempts = 0
    guess = None

    print("Welcome to Guess the Number!")
    print("I'm thinking of a number between 1 and 100.")

    while guess != number_to_guess:
        try:
            guess = int(input("Make a guess: "))
            attempts += 1

            if guess < number_to_guess:
                print("Too low! Try again.")
            elif guess > number_to_guess:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You've guessed the number {number_to_guess} in {attempts} attempts.")
        except ValueError:
            print("Please enter a valid number.")

if __name__ == "__main__":
    guess_the_number()
