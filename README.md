import random

print("""Welcome to the Number Guessing Game!
I'm thinking of a number between 1 and 100.

Please select the difficulty level:
1. Easy (10 chances)
2. Medium (5 chances)
3. Hard (3 chances)""")

diff = input("Choose your difficulty (1-3): ")
a = random.randint(1, 101)  # Random number to guess

def task():
    b = int(input("Choose your number: "))
    if a == b:
        print("You are correct!!")
        return True
    elif a > b:
        print("Too low")
        return False
    else:
        print("Too high")
        return False

if diff == "1":
    print("You have chosen the Easy difficulty")
    for i in range(10):  # 10 chances
        if task():
            break
elif diff == "2":
    print("You have chosen the Medium difficulty")
    for i in range(5):  # 5 chances
        if task():
            break
elif diff == "3":
    print("You have chosen the Hard difficulty")
    for i in range(3):  # 3 chances
        if task():
            break
else:
    print("That is not a difficulty")
#https://roadmap.sh/projects/number-guessing-game
