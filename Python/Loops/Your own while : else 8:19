from random import randint

# Generates a number from 1 through 10 inclusive
random_number = randint(1, 10)
print random_number # for debugging

guesses_left = 3
# Start your game!
while guesses_left > 0:
    guess = int(raw_input("Your guess of number from 1 to 10: "))
    if guess == random_number:
        print 'You win!'
        break
    guesses_left -= 1
    print 'You have', guesses_left, 'guesses left, try again!'
else:
    print 'You lose.'