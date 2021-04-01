# Building a quiz

The objective of this project was to code **a quiz asking three questions to the player**. The latter only has a **limited number of chances**.

## Required libraries

You don't have to install any library or module to run this notebook, as I only used **Python** methods and objects!

## Adaptability

The quiz is composed of **three questions**, and the player has only **three chances**. Feel free to adapt these two parameters!

As questions are **custom**, you can obviously put your own questions as well.

In the bonus part, I suggested a way to implement a **theme selection** for the quiz. I chose themes I like, but these can be adapted to your own tastes!

## Ready-to-use version

The notebook uses a step-by-step approach to build the quiz, but in case you want to have the **final version** of the code you'll find it below.

I excluded the theme selection coded in the bonus part, as it is completely optionnal.

```python
# We will first encapsulate the process of asking a question 
# and verifying the answer given by the player in a function.

def ask_question(nb_attempts_left, question_number, question_sentence, right_answer, text_wrong, text_right):
    if nb_attempts_left > 0:
        print("----------")
        print("Question {}".format(question_number))
        print("----------")
        print()
        
        answer = input(question_sentence)
        
        while answer.lower() != right_answer:
            nb_attempts_left -= 1
            
            if nb_attempts_left == 0:
                print()
                print("Game over...")
                break
            
            if nb_attempts_left == 1:
                print("{} You have 1 chance left.".format(text_wrong))
            else:
                print("{} You have {} chances left.".format(text_wrong, nb_attempts_left))
         
            print()
            answer = input(question_sentence)
    
        if nb_attempts_left != 0:
            print(text_right)
            print()
        
    return nb_attempts_left # This element will navigate throughout the questions.

questions_answers_list = [("1", 
                           "In tennis, how many Grand Slam tournaments are there? ", 
                           "4",
                           "That is not the correct answer, try again!",
                           "There are indeed four Grand Slam tournaments: the Australian Open, Roland-Garros, Wimbledon and the US Open. Good job!"),
                          ("2", 
                           "Which English band is David Gilmour the guitarist of? ", 
                           "pink floyd",
                           "I'm afraid this is a wrong answer, try something else.",
                           "Exactly. Did you know that David Gilmour is not a founding member of the band? He only joined in 1968, three years after its creation, to take Syd Barrett's place."),
                          ("3", 
                           "Which manga narrates the adventures of Straw Hat Pirates? ", 
                           "one piece",
                           "Mmmh, I don't think so...",
                           "You're right! I wonder if this saga will ever end... The first chapter was published in 1997!")]

# Now that we have defined our function and our list, all we have to do is using them.
# We have to define an initial number of chances, which will only be used at the first question.
# Afterwards, the value being used is the one returned by our function, updated according
# to the number of wrong answers given by the player.

nb_attempts = 3

print("Welcome to our quiz!")
print("You have {} lives.".format(nb_attempts)) # Small change here: the text will adapt to the number of chances defined.
print()

for number, question, answer, text_wrong, text_right in questions_answers_list: # We iterate over the elements of our list.
    nb_attempts = ask_question(nb_attempts, number, question, answer, text_wrong, text_right)

if nb_attempts > 0:
    print("Congratulations, you won the quiz!")
```