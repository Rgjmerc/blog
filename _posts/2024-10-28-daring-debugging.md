# Debugging Journey

## Introduction to Debugging

This is the quick rundown of me debugging several lines of code to get them up and running. To understand what im about to say you need to understand debugging first. Debugging is the task of taking a piece of code with bugs or errors and analyzing it to determine the problems still lying in the code and fix them.

Debugging is a tedious task that requires time and precision to complete in a well done manner. If the debugging task doesnt have a majority or your attention then the finished result with more errors than what was originally in the code.

## Debug 1

The Original bugged code for the first task was as follows.
```python
text = "Hello, world, my name is"
count = 0

for char in text:
    if char == "":
       count += 1

print(count)
```
The intention of the code was to count how many spaces are in a given string. Now the issue may not be very noticeable at a first glance as it is a very minor issue that can be fixed with a single character. The issue was that the code was trying to look for nothing since there was nothing in the if char == statement. All that's needed to resolve this issue is to add a space in the if char == string so that the code looks for spaces.

## Debug 2

The bugged code for the second task can be seen below.
```python
print("give me a number")
n = input()

for num in range(1, n):
    if num % 2 < 0:
        print(num, "is even.")
    else:
        print(num, "is odd.")
```
The point of this code was to determine if numbers 1 to n are even or odd. Unlike the previous debugging task this one has several issues in it's code. The problems in this code are that the code states if the number % 2 is < than 0 but that won't determine if the number is even or odd only that the remainder is greater than 0 and the input is rendered as a string. To fix these issues one must change the < sign to the == sign & add an int() before the input.

## Debug 3

The third task's bugged code is below.
```python
num = int(input("Enter an integer: "))

if num < -1:
  print("No negative numbers.")
else:
  result = 1
  for i in range(1, num):
    result *= i   

  print("Factorial of " + num + "is" + result)
```
The original intention of this code was to calculate the factorial of a given number. The errors of this code consisted of the fact that a negative number could still be entered since -1 is not < -1 & the print statement at the end wouldn't function as intended due to the integers. There was a simple solution, and that was to change the -1 to a 0 & make the print into a f string.

## Debug 4

The final task was as follows.
```python
attempts = 0
correct_password = "secret"

while True:
    password = input("Enter your password: ")
    attempts += 1

    if password == "incorrect_password":
        print("Correct password!")
    else:
        print("Incorrect password")

    if attempts > 3:
        print("Too many attempts")
        break
```
It was a bit more difficult solve the issues stated since they were more hidden that the previous code. Dispite this I was still able to find the errors in the code to fix its original function of ask user to enter the correct password but only give them 3 attempts. The errors which needed to be fixed consisted of the actual correct password being “incorrect_password”, the code still looping despite achieving the correct password & the user being given 4 attempts since 3 isn’t > 3. To fix these errors one must change “password == “incorrect_password”” to “password == correct_password”, add a break after the correct password is achieved so the code ends & make attempts >= 3 to stop for too many attempts.