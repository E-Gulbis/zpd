# Es izveidoju 2 spēles ar Python programmēšanas valodu

### Saturs

#### 1. Spēles apraksts

#### 1. Spēles kods

#### 2. Spēles apraksts

#### 2. Spēles kods
---
# 1. spēles apraksts
Dators nejauši izvēlas skaitli no 1 līdz 100, tad spēlētājam tas ir jāuzmin. Dators arī teiks, ja skaitlis ir lielāks par mēģinājumu vai mazāks.

1. Spēles kods:
```py
  from random import randrange
num = randrange(0, 100)
guess = int(input("Guess the number...\n"))
tries = 0
while guess != num:
    tries += 1
    if guess > num:
        guess = int(input("Lower, try again...\n"))
    else:
        guess = int(input("Higher, try again..."))
if tries == 1:
    print("How..?\nYou guessed on the first try!")
elif tries == 0:
    print("How did you win without guessing, cheater?")
else:
    print("You finally guessed %i after %i tries!" % (num, tries))
```

Šis ir diezgan labs, bet tas mēdz apnikt kad to spēlē pārāk daudz (vienu) reizes.
---
# 2. Spēles apraksts
Kāpēc lietot savas rokas un galvu, ja var uzticēt vieglo uzdevumu datoram. Šī ir "akmens šķēres papīrīt's" spēle datorā.

2. Spēles kods
```py
from random import randrange

def check_win():
    if (mann == "r"):
        mann = "rock"
    elif (mann == "p"):
        mann = "paper"
    elif (mann == "s"):
        mann = "scissors"
    print("You played " + mann + " against " + name + "'s " + cpu + "!")
    if(mann == "rock" and cpu == "scissors"):
        gamestate = "win"
    elif(mann == "scissors" and cpu == "paper"):
        gamestate = "win"
    elif(mann == "paper" and cpu == "rock"):
        gamestate = "win"
    elif(mann == "rock" and cpu == "paper"):
        gamestate = "lose"
    elif(mann == "paper" and cpu ==  "scissors"):
        gamestate = "lose"
    elif(mann == "scissors" and cpu == "rock"):
        gamestate = "lose"
    elif(mann == cpu):
        gamestate = "draw"
    if(gamestate == "win"):
        print("You won! Well done!")
    elif(gamestate == "lose"):
        print("You lost. For shame!")
    elif(gamestate == "draw"):
        print("It's the stalest mate I've seen.")
    elif(gamestate == "ERROR!"):
        print("Something went wrong - don't cry.")
        print("mann = " + mann + ", cpu = " + cpu)
    print("GG, now sod off.\n")
mode = input("Are you playing alone? (y/n): ")
gamestate = "ERROR!"
if(mode == "y"):
    print("Welcome to rock paper scissors: man vs machine!")
    mann = input("Choose your weapon (rock/paper/scissors) or (r/p/s) ")
    if (mann == "rock" or mann == "r"):
        print("You chose rock!\n")
    elif (mann == "paper" or mann == "p"):
        print("You chose paper!\n")
    elif (mann == "scissors" or mann == 's'):
        print("You chose scissors!\n")
    elif (mann == "gun"):
        print("NUH UHHH!!!")
    else:
        print("Bruh moment - that's not an option")
    thonk = input("Would you like to name your enemy? (y/n) ")
    if(thonk == "y"):
        name = input("What would you like to name your enemy?\n")
        print("You'll fight " + name + ".")
    else:
        print("You'll fight your imaginary friend.\n")
        name = "imaginary friend"
    cpu = randrange(3)
    if(cpu == 0):
        cpu = "rock"
    elif(cpu == 1):
        cpu = "paper"
    else:
        cpu = "scissors"
    if mann != "gun":
        check_win()
    else:
        print("You were killed by security. Your corpse rots in a back alley.")
elif(mode == "n"):
    name1 = input("What's the name of the first player?\n")
    name2 = input("\nWhat's the name of the second player?\n")
    print("Prepare to make your choices!")
    print(name1 + ", make your choice - make sure that no one is looking over your shoulder.")
    p1 = input("choose (r/p/s): ")
    if (p1 == "r"):
        p1 = "rock"
    elif (p1 == "p"):
        p1 = "paper"
    elif (p1 == "s"):
        p1 = "scissors"
    print("\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\nNow " + name2 + "!")
    p2 = input("choose (r/p/s): ")
    if (p2 == "r"):
        p2 = "rock"
    elif (p2 == "p"):
        p2 = "paper"
    elif (p2 == "s"):
        p2 = "scissors"
    print("\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n")
    if(p1 == "rock" and p2 == "scissors"):
        gamestate = "win"
    elif(p1 == "scissors" and p2 == "paper"):
        gamestate = "win"
    elif(p1 == "paper" and p2 == "rock"):
        gamestate = "win"
    elif(p1 == "rock" and p2 == "paper"):
        gamestate = "lose"
    elif(p1 == "paper" and p2 ==  "scissors"):
        gamestate = "lose"
    elif(p1 == "scissors" and p2 == "rock"):
        gamestate = "lose"
    elif(p1 == p2):
        gamestate = "draw"
    if(gamestate == "win"):
        print(name1 + " wins!")
    elif(gamestate == "lose"):
        print(name2 + " wins!")
    elif(gamestate == "draw"):
        print("It's the stalest mate I've seen.")
    elif(gamestate == "ERROR!"):
        print("Something went wrong - don't cry.")
        print("p1 = " + p1 + ", p2 = " + p2)
    print("GG, now sod off.\n")
else:
    print("read the brackets, dumdum. you answered " + mode)
```
Spēle ir angliski, jo esmu pieradis tajā valodā rakstīt.
