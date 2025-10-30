import random

options = ("rock", "paper", "scissors")

winning_combos = {
    "rock:scissors": "You Win!",
    "paper:rock": "You Win!",
    "scissors:paper": "You Win!",
    "scissors:rock": "You Lose!",
    "rock:paper": "You Lose!",
    "paper:scissors": "You Lose!"
}

humanscore = 0
robotscore = 0

while True:
    userplay = input("Do you want to play RPS (Y/N)? ").upper()
    if userplay == "Y":
        humanchoice = input("Enter rock, paper or scissors: ").lower()

        if humanchoice not in options:
            print("That's not an option!")
            continue
            

        robotchoice = random.choice(options)
        print(f"The robot chose: {robotchoice}")

        if humanchoice == robotchoice:
            print("It's a draw!")
            humanscore += 0.5
            robotscore += 0.5

        elif f"{humanchoice}:{robotchoice}" in winning_combos:
            result = winning_combos.get(f"{humanchoice}:{robotchoice}")
            print(result)
            if result == "You Win!":
                humanscore += 1
            elif result == "You Lose!":
                robotscore += 1
        else:
            print("Error404")

    elif userplay == "N":
        break
    else:
        print("Y or N")

print(f"""Robot's Score: {robotscore:.1f}
Human's Score: {humanscore:.1f}""")
