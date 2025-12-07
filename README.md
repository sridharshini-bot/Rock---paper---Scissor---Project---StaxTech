# Rock---paper---Scissor---Project---StaxTech
import random

def get_user_choice():
    """Prompt the user to enter rock, paper, or scissors."""
    choice = input("Enter your choice (rock, paper, scissors): ").lower()
    while choice not in ["rock", "paper", "scissors"]:
        print("Invalid choice! Please try again.")
        choice = input("Enter your choice (rock, paper, scissors): ").lower()
    return choice

def get_computer_choice():
    """Randomly select rock, paper, or scissors for the computer."""
    return random.choice(["rock", "paper", "scissors"])

def determine_winner(user, computer):
    """Determine the winner based on classic rules."""
    if user == computer:
        return "It's a tie!"
    elif (user == "rock" and computer == "scissors") or \
         (user == "scissors" and computer == "paper") or \
         (user == "paper" and computer == "rock"):
        return "You win!"
    else:
        return "Computer wins!"

def play_game():
    """Main function to play Rock-Paper-Scissors."""
    print("=== Rock-Paper-Scissors Game ===")
    user_choice = get_user_choice()
    computer_choice = get_computer_choice()
    
    print(f"\nYou chose: {user_choice}")
    print(f"Computer chose: {computer_choice}")
    
    result = determine_winner(user_choice, computer_choice)
    print(result)


if __name__ == "__main__":
    play_game()
