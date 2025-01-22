# python-quiz
This is a python program which randomly asks math,riddles and general knowledge questions.
import random
general_knowledge = {
    "What is the capital of India?": "Delhi",
    "Who painted the Mona Lisa?": "Leonardo da Vinci",
    "What is the largest planet in our solar system?": "Jupiter",
    "What is the chemical symbol for gold?": "Au",
    "Who wrote the play 'Romeo and Juliet'?": "William Shakespeare",
    "What is the tallest mountain in the world?": "Mount Everest",
    "What is the currency of Japan?": "Yen",
    "Who discovered penicillin?": "Alexander Fleming",
    "What is the largest ocean in the world?": "Pacific Ocean",
    "What is the smallest country in the world?": "Vatican City",
    "What is the largest mammal in the world?": "Blue Whale",
    "What is the capital of Australia?": "Canberra",
    "Who is the author of 'To Kill a Mockingbird'?": "Harper Lee",
}
riddles = {
    "I am always hungry, I must always be fed. The finger I touch, will soon turn red. What am I?": "Fire",
    "What has keys but can't open locks?": "Piano",
    "What has a heart that doesn't beat?": "Artichoke",
    "What has a head and a tail but no body?": "Coin",
    "What has a neck but no head?": "Bottle",
    "What has a face and two hands, but no arms or legs?": "Clock",
    "What has a thumb and four fingers, but is not a hand?": "Glove",
    "What has a head and a tail, but no body?": "Coin",
    "What has a heart that doesn't beat?": "Artichoke"
}
math = {
    "What is the square root of 64?": "8",
    "What is the value of pi (to two decimal places)?": "3.14",
    "What is the value of e (to two decimal places)?": "2.71",
    "What is the value of the number 'infinity'?": "Infinity",
    "What is the value of the number 'not a number'?": "NaN",
    "What is the value of the number 'zero'?": "0",
    "What is the value of the number 'one'?": "1",
    "What is the value of the number 'two'?": "2",
    "What is the value of the number 'three'?": "3",
    "What is the value of the number 'four'?": "4",
    "What is the value of the number 'five'?": "5",
    "What is the value of the number 'six'?": "6",
    "What is the value of the number 'seven'?": "7",
    "What is the value of the number 'eight'?": "8",
}
def ask_question(category):
    question,answer = random.choice(list(category.items()))
    print(question)
    score = 0
    user_answer = input("Your answer: ")
    if user_answer.lower() == answer.lower():
        print("Correct!")
        return True
        score=+1

    else:
        print("Incorrect. The correct answer is:", answer)
        return False,score


    print()

def quiz_game():
    print("Welcome to quiz game")
total_score = 0
while True:
    print("1.general_knowledge\n",
           "2.riddles\n",
            "3.math\n",
            "4.quit\n")
    choice = str(input("enter your choice from (1-4)\n"))
    if choice == "1":
       print("\ngeneral_knowledge question")
       total_score += ask_question(general_knowledge) 

    elif choice == "2":
        print("\nRiddles:")
        total_score += ask_question(riddles)  
    elif choice == "3":
        print("\nMath Questions:")
        total_score += ask_question(math)  
    elif choice == "4":
           
        print(f"\nThank you for playing! Your total score is{total_score}.")
        break
    else:
            
        print("Invalid choice. Please try again.")
        print(f"Your current score is: {total_score}")
