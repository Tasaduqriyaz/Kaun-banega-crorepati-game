# Kaun-banega-crorepati-game
# I have tried to create a replica of famous Indian game show KBC 
questions = [
    ['Who was our first president ?','A ABUL KALAM', 'B JAHANGIR KHAN', 'C RAJENDRA PRASAD','D INDIRA GANDHI','E NONE',3],
    ['Who invented telephone ?','A GRAHAM BELL', 'B VALKONOSKI', 'C NEWTON','D TESLA','E NONE',1],
    ['Who of these is a browser ?','A OPERA', 'B DELIOTTE', 'C ACCENTURE','D KNIFE','E NONE',1],
    ['Who of these have highest speed ?','A SOUND', 'B LIGHT', 'C METALS','D NON-METALS','E NONE',2],
    ['Who is undefeated in UFC ?','A CHARLES OLEVERIA', 'B ISLAM MAHACHOV', 'C KHABIB','D DC','E NONE',3],
    ['Which of these is a prime number?','A 2', 'B  9', 'C 18','D 56','E NONE',1],
    ['Which of these is a fruit ?','A ORANGE', 'B GOURD', 'C CARROT','D LADYFINGER','E NONE',1],
    ['Who of these is not a phone ?','A APPLE', 'B SAMSUNG', 'C CHERRY','D LG','E NONE',3],
    ['Which of these is not a programming language ?','A  C', 'B PYTHON', 'C JAVA','D TALLY','E NONE',4],
    ['Who is current president of united states?','A BARACK OBAMA', 'B JOE BIDEN', 'C HILARY CLINTON','D GOORGE BUSH','E NONE',2],
    ['Who is the richest man ?','A STEVE JOBS', 'B MARK ZUCKERBERG', 'C ELON MUSK','D BILL GATES','E NONE',3],
    ['Who is the CEO of boat ?','ANUPAM MITTAL', 'B AMAN GUPTA', 'C PIYUSH BANSAL','D AZHAR','E NONE',2],
    ['Who is the richest actor ?','A SRK', 'B SALMAN', 'C AAMIR','D AKHSAY','E NONE',1],
    ['Who is the richest cricketer ?','A SACHIN', 'B KOHLI', 'C DHONI','D RAINA','E NONE',3],
    ['Who is the fastest athelete ?','A CR7', 'B USAIN BOLT', 'C MESSI','D POLLARD','E NONE',2]
]
Levels = [1000,2000,3000,5000,10000,20000,40000,80000,160000,320000,640000,1250000,2500000,5000000,10000000]
i= 0
money =0
run_once = 0
for i in range(0,len(questions)):
    question = questions[i]
    print (f'Here is your question for Rs.{Levels[i]}')
    print('\n')
    print (question[0])
    print (f'{question[1]}                  {question[2]}')
    print (f'{question[3]}              {question[4]}')
    print (f'{question[5]}')
    reply = int(input('enter the value between 1-4 ,0 for quitting, 6 FOR 50-50'))
    print ('\n')
    if reply==0:
      money=Levels[i-1]
      break
    if run_once ==0:
        if reply==6:  
           answer =question[question[-1]] 
           answer2= question[question[-1] -6]
           print(f'{answer}                          {answer2}')                       
           reply = int(input('enter the value between 1-4 ,0 for quitting')) 
           run_once =1  
    if reply == question[-1]:
        print (f'correct answer! You have won Rs.{Levels[i]}')
        if i==4:
            money = 10000
        if i==9:
           money = 320000
        if i==14:
          money = 10000000
          print('You are a crorepati')
    else:
     print ('wrong answer! you have lost the game')
     break
print (f'The total amount of money won is Rs.{money}')
