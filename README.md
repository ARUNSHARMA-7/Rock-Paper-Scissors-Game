<img width="1012" height="510" alt="image" src="https://github.com/user-attachments/assets/f7b99eda-8cc0-4270-aa61-c4f5dc5b8682" />
import random
options = ["rock", "paper", "scissors"]
while True:
    user_choice = input("Enter rock, paper or scissors (or 'exit' to quit): ").lower()
    if user_choice == "exit":
        print("Game Over. Thanks for playing!")
        break
    if user_choice not in options:
        print("Invalid choice, try again.")
        continue
    
    computer_choice = random.choice(options)
    print("Computer chose:", computer_choice)
    
    if user_choice == computer_choice:
        print("It's a tie!")
    elif (user_choice == "rock" and computer_choice == "scissors") or \
         (user_choice == "paper" and computer_choice == "rock") or \
         (user_choice == "scissors" and computer_choice == "paper"):
        print("You win!")
    else:
        print("Computer wins!")
