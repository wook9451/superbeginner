# superbeginner
from random import randrange

X = {'ga':0,'ba':1,'bo':2}
X1 = {v:k for k,v in X.items()}

R_me, R_com = 0, 0

while R_me < 3 and R_com< 3:
    a = input()
    if a not in X:
        print('NO')
        continue
    b = randrange(3)

    r_me = ((X[a] - b) % 3) % 2
    r_com = ((b - X[a]) % 3) % 2
    R_me += r_me
    R_com += r_com

    print('Com:',X1[b],end="   ")
    print('You win!' if r_me else ('You lose!' if r_com else 'Draw!'), end='')
    print('%s : %s' %  (R_me,R_com))
 

if R_me>R_com:
    print("Congraturation!! You win the game! The final score is %s : %s" % (R_me, R_com) )  
else:
    print("Unfortunately, You lose the game. The final score is %s : %s" % (R_me, R_com) )  

