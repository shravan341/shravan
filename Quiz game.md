# Quiz Game
#You have to build a dictionary (Or any other container of your choice) which contains multiple 
# True/false type quiz questions.
# Every participant/user will attempt 5 rounds and in each round random quiz questions will be 
# displayed to the user/participant.
# If the participant answers the quiz question correct, then congratulate him and add the scores.
# At the end display the details and score of the participant


question = {"In school, Albert Einstein failed most of the subjects, except for physics and math.": "Yes",
            "The first song ever sung in the space was Happy Birthday.": "Yes",
            " A male canary tends to have a better singing voice than a female canary.": "Yes",
            "Tea contains more caffeine than coffee and soda": "No",
            "Dogs have an appendix.": "No",
            "Bill Gates is the founder of Amazon.": "No",
            "Mice have more bones than humans.": "Yes",
            "The first product with a bar code was chewing gum": "Yes",
            "The Beatles is a famous rock band from Manchester, the United Kingdom": "No",
            "The star is the most common symbol used in all national flags around the world.": "Yes"}  
import random

questionlist = []
while (len(questionlist) != 5):  
    i = random.choice(list(question.keys()))  
    if (i not in questionlist):
        questionlist.append(i)  
score = 0
print("""888888""")
for i in questionlist:
    print("\n" + i)
    a = input("\nEnter Yes or No: ")
    if (a == question[i]):
        print("\nRight answer! +5 points")
        score += 5
    else:
        print("\nWrong answer!")
print("\nTotal Score is :", score)
