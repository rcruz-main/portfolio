import random


def main():
    show_header()
    play_game()


def show_header():
    print("-------------------------------")
    print("      M&M guessing game!")
    print("-------------------------------")
    print()


def play_game():
    global mm_count
    global attempt_limit
    global attempts
    global guess

    mm_count = random.randint(1, 100)
    attempt_limit = 5
    attempts = 0

    print(f"Guess the number of M&Ms in {attempt_limit} attempts and you get lunch on the house!")
    print()

    while attempts < attempt_limit:
        guess_text = input("How many M&Ms are in the jar?")
        guess = int(guess_text)
        attempts += 1

        if guess == mm_count or attempts == attempt_limit:
            check_winner()
            break

        elif mm_count < guess:
            print(f"{guess} is High!")

        elif mm_count > guess:
            print(f"{guess} is Low!")


def check_winner():
    if attempts == 1:
        print(
            f"I'm impressed you got in 1 try! Bonus dessert on the house aside from lunch! There are {guess} M&Ms in "
            f"the Jar!")

    elif mm_count != guess:
        print(f"Sorry, you've guessed {attempts} times already. Right answer is {mm_count}")

    else:
        print(f"You got it right in {attempts} tries! There are {guess} M&Ms in the Jar!")
        print("Your lunch is on the house!")


if __name__ == '__main__':
    main()
