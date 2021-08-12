# Helpp
cube = float(input("Hay nhap 1 so: "))
epsilon = 0.0001
num_guess = 0
if cube == 0:
    guess = 0
elif cube == 1:
    guess = 1
elif cube < 0:
    low = cube
    high = 0
    guess = (low + high)/2
    while abs(guess**3 - cube) >= epsilon:
        num_guess += 1
        if guess ** 3 < cube:
            low = guess
        else:
            high = guess
        guess = (low + high)/2
elif cube > 1:
    low = 0
    high = cube
    guess = (low  + high)/2
    while abs(guess**3 - cube) >= epsilon:
        num_guess += 1
        if guess**3 < cube:
            low = guess
        else: 
            high = guess 
        guess = (low + high)/2
elif 0 < cube < 1:
    low = 0
    high = 1/cube
    guess = (low + high)/2
    while abs(guess**3 - 1/cube) >= epsilon:
        num_guess += 1
        if guess ** 3 < 1/cube:
            low = guess
        else:
            high = guess
        guess = (low + high)/2
    guess = 1/guess    
else:
    low = 1/cube
    high = 0
    guess = (low + high)/2
    while abs(guess**3 - 1/cube) >= epsilon:
        num_guess += 1
        if guess**3 < 1/cube:
            low = guess
        else:
            high = guess
        guess = (low + high)/2
    guess = 1/guess
print ("Can bac 3 cua", cube, "la:", guess)
print ("So lan doan la:", num_guess)
