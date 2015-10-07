# Basic-Python-Projects
#Coursera class

#Week 1 project

print "We want... a shrubbery!"





#Week 2 project (Rock-Paper-Scissors-Lizard-Spock)

# Let's play Rock, Paper, Scissors, Lizard, Spock!

import random

def name_to_number(name):   
    if name.lower() == "rock": 
        return 0
    elif name.lower() == "spock":
        return 1
    elif name.lower() == "paper":
        return 2
    elif name.lower() == "lizard":
        return 3
    elif name.lower() == "scissors":
        return 4
    else:        
        print name + " is not an appropriate choice"

        
def number_to_name(number):
    if number == 0:
        return "rock"
    elif number == 1:
        return "spock"
    elif number == 2:
        return "paper"
    elif number == 3:
        return "lizard"
    elif number == 4:
        return "scissors"
    else:
        print name + " is not an appropriate choice"

def rpsls(player_choice):
    print ""
    print "Player chooses " + player_choice
    player_number = name_to_number (player_choice)
    comp_number = random.randrange(0,4)
    comp_choice = number_to_name(comp_number)
    print "Computer chooses " + comp_choice
    # compute difference of comp_number and player_number modulo five
    (comp_number - player_number) %5  
    if player_number == 0:
        if comp_number == 3 or comp_number == 4:
            return "Player Wins!"
        elif comp_number == 1 or comp_number == 2:
            return "Computer Wins!"
        else:
            return "Player and computer tie!"
    if player_number == 1:
        if comp_number == 4 or comp_number == 0:
            return "Player Wins!"
        elif comp_number == 2 or comp_number == 3:
            return "Computer Wins!"
        else:
            return "Player and computer tie!"
    if player_number == 2:
        if comp_number == 0 or comp_number == 1:
            return "Player Wins!"
        elif comp_number == 3 or comp_number == 4:
            return "Computer Wins!"
        else:
            return "Player and computer tie!"
    if player_number == 3:
        if comp_number == 1 or comp_number == 2:
            return "Player Wins!"
        elif comp_number == 0 or comp_number == 4:
            return "Computer Wins!"
        else:
            return "Player and computer tie!"
    if player_number == 4:
        if comp_number == 2 or comp_number == 3:
            return "Player Wins!"
        elif comp_number == 0 or comp_number == 1:
            return "Computer Wins!"
        else:
            return "Player and computer tie!"
    
print rpsls("rock")
print rpsls("Spock")
print rpsls("paper")
print rpsls("lizard")
print rpsls("scissors")


#Rules:
#Rock smashes scissors and Lizard 
#	it gets covered by paper and vaporized by Sprock
#Spock smashes scissors and vaporizes rock 
#   he is poisoned by lizard and disproven by paper
#Paper covers rock and disproves Sprock
#	it gets eaten by Lizard and cut up by scissors 
#Lizard poisons Spock and eats paper
#   it is crushed by rock and decapitated by scissors 
#Scissors cuts paper and Lizard
#   it gets smashed by rock and Sprock




#Week 3 (Incomplete; Guess the number game)

import random
import simplegui
import math

secret_number = random.randrange(0,100)
secret_number2 = random.randrange(0,1000)

def input_guess(guess):
    return int(guess)
    print "Guess was ", str(guess), "."

def new_game():
    global secret_number

num_range = 100

def range100():
    global secret_number
    
    f.add_button("Range is from 0 to 100", range100)
    
new_game()

num_range = 1000

def range1000():
    global secret_number2
    f.add_button("Range is from 0 to 1000", range1000)    

new_game()


def input_guess(guess):
    global secret_number
    if guess is < secret_number:
        return "The number is smaller"
        print "By Thor's hammer, you got it!"
    else:
        print "You got it wrong... but never give up, never surrender."

def output(secret_number):
    if input_guess is output:
        return True
        print "By Thor's hammer, you got it!"
    else:
        print "You got it wrong... but never give up, never surrender."


f = simplegui.create_frame("Guess that number", 200, 200)
f.set_canvas_background("Green")

f.start()

f.add_button("Range is 0 to 100", range100, 200)
f.add_button("Range is from 0 to 1000", range1000, 200)
f.add_input("Enter a guess", input_guess, 200)
             
new_game()


