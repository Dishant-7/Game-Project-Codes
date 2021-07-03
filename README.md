# Rock-Paper-and-Scissor-Game-using-Python
<!-- Create the game of Rock, Paper and Scissor using some really easy concepts of Python like if.....else if.....else and loops. -->
import random
while True:
    print('welcome to game')
    Choices=['rock','paper','scissor']
    computer_choice = str(random.choice(Choices))
    print('computer has selected', computer_choice)
    your_score=0
    computer_score=0
    for i in range(1,6):
        print('round ',i)
        your_choice = int(input('enter your choice'))

        if(your_choice==1):
            print('you have selected rock')
            your_choice='rock'
        elif(your_choice==2):
            print('you have selected paper')
            user_choice='paper'
        elif(your_choice==3):
            print('your choice is scissor')
            your_choice='scissor'
        else:
            print('invalid choice please select again')
            break
        if(your_choice==computer_choice):
            print('round draw')
        if((your_choice=='rock' and computer_choice=='scissor')
                or (your_choice=='paper' and computer_choice=='rock')
                or (your_choice=='scissor' and computer_choice=='paper')):
            print('user wins this round')
            your_score=your_score+1
        elif((your_choice=='scissor' and computer_choice=='rock')
                or (your_choice=='rock' and computer_choice=='paper')
                or (your_choice=='paper' and computer_choice=='scissor')):
            print('computer wins this round')
            computer_score=computer_score+1

        if(your_score>computer_score):
            print('you win')
        elif(your_score<computer_score):
            print(('computer wins'))
        else:
            print('match draw')
        print('do you want to play again')
        response=input('yes or no')
        if(response=='yes'):
            continue
        else:
            break
