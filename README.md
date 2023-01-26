# assignment-4
#Ans1
# Prompt the user to enter their marks
marks = int(input("Enter your marks: "))

# Determine the corresponding grade based on the rules provided
if marks < 25: # Marks below 25
    grade = "F"
elif marks >= 25 and marks < 45: # Marks between 25 and 45
    grade = "E"
elif marks >= 45 and marks < 50: # Marks between 45 and 50
    grade = "D"
elif marks >= 50 and marks < 60: # Marks between 50 and 60
    grade = "C"
elif marks >= 60 and marks < 80: # Marks between 60 and 80
    grade = "B"
else: # Marks above 80
    grade = "A"

# Print out the grade
print("Your grade is:", grade)
#Ans2
year = input("Enter a year: ")
year = int(year)

# check if the year is divisible by 4
if year % 4 == 0:
   # if the year is divisible by 4, check if it is divisible by 100
   if year % 100 == 0:
       # if the year is divisible by 100, check if it is also divisible by 400
       if year % 400 == 0:
           # if the year is divisible by 400, it is a leap year
           print(year, "is a leap year")
       else:
           # if the year is not divisible by 400, it is not a leap year
           print(year, "is not a leap year")
   else:
       # if the year is not divisible by 100, it is a leap year
       print(year, "is a leap year")
else:
   # if the year is not divisible by 4, it is not a leap year
   print(year, "is not a leap year")
Footer
#Ans 3
import random

# generate ten random multiplication questions
for i in range(10):
   # generate two random numbers between 1 and 9
   num1 = random.randint(1, 9)
   num2 = random.randint(1, 9)

   # compute the correct answer
   answer = num1 * num2

   # ask the player to solve the question
   guess = input(f"Question {i+1}: {num1} x {num2} = ")
   guess = int(guess)

   # check if the player's guess is correct
   if guess == answer:
       print("Right!")
   else:
       print(f"Wrong. The answer is {answer}.")
   #Ans 4
   # start with the lowest possible number of pieces
pieces = 1

# keep looping until we find the correct number of pieces
while True:
   # check if the number of pieces is divisible by 5, 6, and 7
   if pieces % 5 == 2 and pieces % 6 == 3 and pieces % 7 == 2:
       # if the number of pieces is divisible by 5, 6, and 7, we have found the correct number of pieces
       break

   # if the number of pieces is not divisible by 5, 6, and 7, try the next number
   pieces += 1

   # stop if the number of pieces is greater than 200
   if pieces > 200:
       break

# print the number of pieces
print("The number of pieces is", pieces)
