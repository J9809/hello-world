# GUESS THE NUMBER

import random
a = random.randint(1, 20)
count = 1
i = 5
while i > 1:
  print("You have {} chances left. Guess the number between 1 and 20: ".format(5-count))
  k = int(input())
  if k > a:
    print("Down")
    count += 1
    i -= 1
    continue
  elif k < a:
    print("Up")
    count += 1
    i -= 1
    continue
  else:
    print("Congratulation! You got the number only {} times.".format(count))
    break
if i == 1:
  print("Sorry. The correct number is {}.".format(a))
