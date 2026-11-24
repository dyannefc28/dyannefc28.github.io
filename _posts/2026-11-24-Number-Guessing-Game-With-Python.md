---
layout: post
title: Number Guessing Game
image: "/posts/number-guess.jpg"
tags: [Python, Numpy, Number Guess]
---

In this post I'm going to run through how I've built a number guessing game in Python. 

Let's get into it!

---

Let's first start by importing the random module, which generates the random numbers

```ruby
import random 
```

There's a function within the random module called "randint", which provides two random integers within two bounds

```ruby
random.randint(1,10)
```

In this case, this will generate a random integer between 1 and 10. But let's set some parameters.

```ruby
LOWER_BOUND = 1
UPPER_BOUND = 100
GUESS_LIMIT = 5
GUESS_COUNTER = 0
CORRECT_NUMBER = random.randint(LOWER_BOUND, UPPER_BOUND)
```

This means that the correct number will be between 1 and 100 and the user gets 5 guesses. 
Now, let's add some logic that would increment the guess counter.

```ruby

print(f"Try guessing the number that I'm thinking. It is between {LOWER_BOUND} and {UPPER_BOUND}. Good luck, you have {GUESS_LIMIT} guesses.")

while True:
    user_guess = int(input("What's your guess?"))
    GUESS_COUNTER += 1 
    remaining_guesses = GUESS_LIMIT - GUESS_COUNTER
          
    if LOWER_BOUND <= user_guess <= UPPER_BOUND:
        
        if user_guess == CORRECT_NUMBER:
            print(f"Wow, you got it in {GUESS_COUNTER} guesses - well done!")
            break
        elif user_guess < CORRECT_NUMBER:
            print(f"Your guess is too low, try again! Guesses remaining: {remaining_guesses}")
        else:
            print(f"Your guess is too high, try again!Guesses remaining: {remaining_guesses}")
    else:
        print(f"Your guess is outside the range, try a guess between {LOWER_BOUND} and {UPPER_BOUND}. Guesses remaining: {remaining_guesses}")
    if remaining_guesses == 0:
        print(f"Sorry, you're out of guesses. The number you were after was {CORRECT_NUMBER}")
        break
```


Example output: 

```ruby
Try guessing the number that I'm thinking. It is between 1 and 100
What's your guess? 10
Your guess is too low, try again! Guesses remaining: 4
What's your guess? 20
Your guess is too low, try again! Guesses remaining: 3
What's your guess? 30
Your guess is too high, try again!Guesses remaining: 2
What's your guess? 21
Your guess is too low, try again! Guesses remaining: 1
What's your guess? 22
Your guess is too low, try again! Guesses remaining: 0
Sorry, you're out of guesses. The number you were after was 23
```

