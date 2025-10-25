import random
from art import logo
print(logo)

print("Welcome to thye Number Guessing Game!")
print("I'm thinking of a number between 1 and 100.")

#pull a random number to be the guessed number
correct_guesses = random.randint(1, 100)

# create a value outside to function to store the random number
attempts = 0

# create a function where is storing all the steps to guess the number
def easy_guess():
    # choosing the level
    if user_choise == 'easy':
        # setting the level with the requested attempt by level
        attempts = 10
        # printing the number of the starting attempts reflecting the level
        print(f"You have {attempts} remaining to guess the number.")
        # a loop was created to check if the attepts are greater than 0 to continue running
        while attempts > 0:
            # asking the player to make the first guess
            user_number = int(input("Make a guess: "))
            # setting the parameters if the player number is grater, lower or (else) equal to the random number chose
            if user_number > correct_guesses:
                print("Your guess is too high.")
                # print('Guess again')

                # print(f"You have {attempts} remaining to guess the number.")
            elif user_number < correct_guesses:
                print("Your guess is too low.")
                # print('Guess again')

                # print(f"You have {attempts} remaining to guess the number.")
            else:
                print("You have guessed the correct number.")

                # stop the loop if the player guessed the number
                break

            # decreasing the started attempts by 1 if the random number was not guessed
            attempts -= 1

            # If still are attempts left, the player will be asked again to choose a number
            if attempts > 0:
                print("Guess again.")
                print(f"You have {attempts} remaining to guess the number.")

            # if NO attempts are left player will be informed about that and the random/secret number will be displayed
            else:
                print(f"You are out of the attempts! The correct number was: {correct_guesses}")




# create a function where is storing all the steps to guess the number
def hard_guess():

    # choosing the level
    if user_choise == 'hard':

        # setting the level with the requested attempts by level
        attempts = 5

        # printing the number of the starting attempts reflecting the level
        print(f"You have {attempts} attempts remaining to guess the number.")

      #a loop was created to check if the attempts are greater than 0 to continue running
    while attempts > 0:

        # asking the player to make the first guess
        user_number = int(input("Make a guess: "))

        # setting the parameters if the player number is grater, lower or (else) equal to the random number chosen
        if user_number > correct_guesses:
            print("Your guess is too high.")

        elif user_number < correct_guesses:
            print("Your guess is too low.")


        else:
            print("You got it, The answer was: {correct_guesses}.")

            #stop the loop if the player guessed the number
            break

            #decreasing the started attempts by 1 if the random number was not guessed
        attempts -= 1

            #If still are attempts left, the player will be asked again to choose a number
        if attempts > 0:
                print("Guess again.")
                print(f"You have {attempts} attempts remaining to guess the number.")

            #if NO attempts are left player will be informed about that and the random/secret number will be displayed
        else:
                print(f"You are out of the attempts! The correct number was: {correct_guesses}")

# Asking the player for a number between 1 and 100
user_choise = input("Choose a difficulty level. Type 'easy' or 'hard': ")



#calling (activating) the function for each level
easy_guess()
hard_guess()





