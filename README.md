# GAME-OF-STONE-PAPER-AND-SCISSORS
For creating a simple implementation of Rock-Paper-Scissors



import random

def game():
    while True:
        user = input("Enter your choice (rock/paper/scissors) or 'q' to quit: ").lower()
        if user == 'q':
            break

        if user not in ['rock', 'paper', 'scissors']:
            print("Invalid input. Please try again.")
            continue

        choices = ['rock', 'paper', 'scissors']
        computer = random.choice(choices)

        print(f"\nComputer chose: {computer}")

        if user == computer:
            print(f"Both players selected {user}. It's a tie!")
        elif user == 'rock':
            if computer == 'scissors':
                print("Rock smashes scissors! You win!")
            else:
                print("Paper covers rock! You lose.")
        elif user == 'paper':
            if computer == 'rock':
                print("Paper covers rock! You win!")
            else:
                print("Scissors cuts paper! You lose.")
        elif user == 'scissors':
            if computer == 'paper':
                print("Scissors cuts paper! You win!")
            else:
                print("Rock smashes scissors! You lose.")

game()


This code will keep running until you enter 'q' to quit. It asks for your choice, generates the computer's choice, and determines the winner based on the game's rules.
