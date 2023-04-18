# stone_paper_scissor_game
#This is a beginner level game using python 
#using conditions,random  and faction 
import random

def gamewin(computer,you):
    if computer==you:
        return None
    elif computer=="S":
        if you=="C":
            return False
        elif you=="P":
            return True
    elif computer=="C":
        if you=="P":
            return False
        elif you=="S":
            return True 
    elif computer=="P":
        if you=="S":
            return False
        elif you=="C":
            return True   
print("computer Turn: STONE(S) PAPER(P) or SCISSOR(C)?")
randno=random.randint(1,3)
if randno==1:
    computer="S"
elif randno==2:
    computer="C"
elif randno==3:
    computer="P"

you=input("your's Turn: STONE(S) PAPER(P) or SCISSOR(C)?")

a=gamewin(computer,you)
if a==None:
    print("DRAW MATCH !!!!")
elif a:
    print("YOU WIN !!!")
else:
    print("YOU LOSE !!!")
