# jubilant-octo-chainsaw
Number Guessing Game
#Project (Beginner)


import random
# Hello.py - A simple age guessing game
number = 18
attempts = 3
print("Can you guess my age? I will give you 3 attempts.")

while attempts > 0:
    guess_input = input("Enter your guess: ")
    if not guess_input.isdigit():
        print("Please enter a valid number.")
        continue
    guess = int(guess_input)
    if guess == number:
        print("Congratulations! You guessed my age correctly!")
        break
    elif guess < number:
        print("Not quite, but your guess is too low:", attempts - 1)
    else:
        print("Too high! You have", attempts - 1, "attempts left.")
    attempts -= 1

if attempts == 0:
    print("Sorry, you've run out of attempts. My age is:", number)
print("Thanks for playing!")
