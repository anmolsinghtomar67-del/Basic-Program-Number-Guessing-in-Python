import random
def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 1 and 100.")
    number_to_guess = random.randint(1, 100)
    attempts = 0
    while True:
        user_guess = input("Please enter your guess (or type 'exit' to 'quit)")
        if user_guess.lower() == 'exit':
            print("Thanks for playing! Goodbye.")
            break
        try:
            user_guess = int(user_guess)
            attempts += 1
            if user_guess < number_to_guess:
                print("Too low! Try again.")
            elif user_guess > number_to_guess:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You've guessed the number {number_to_guess} in {attempts} attempts.")
                break
        except ValueError:
            print("Please enter a valid number.")
            print("If you want to exit the game, type 'exit'.")
            print("Let's try again.")
