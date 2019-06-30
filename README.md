# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**

for question1 in 1...150 {
print("\(question1)")
}

***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

for question2 in 142..<160 {
print("\(question2)")
}

***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

let question3 = 15...80

for evenNums in question3 where (evenNums % 2 == 0)
{
print (evenNums)
}



***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

let question4 = 19...51

for oddNums in question4 where (oddNums % 2 != 0)
{
print (oddNums)
}



***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

let question5 = 1..<101

for fives in question5 where (fives % 10 == 5)
{
print (fives)
}




***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

let question6 = 1...40

for sevens in question6 where (sevens % 10 == 7)
{
print (sevens)
}




***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

let question7 = 20...150

for threes in question7 where (threes % 3 == 0)
{
print (threes)
}



***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`

let question8 = 20...150

for twoThree in question8 where (twoThree % 2 == 0) && (twoThree % 3 == 0)
{
print (twoThree)
}



***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

let question9 = 20...150

for endFour in question9 where (endFour % 10 == 4)
{
print (endFour)
}


***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

let question10 = 20...150

for exactNums in question10 where (exactNums == 31) || (exactNums == 35) || ((exactNums > 39) && (exactNums < 61))
{
print (exactNums)
}


***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
i += 1
}

// Your explanation here
```

this will be an infinite loop becase there is no case that will prove to be false because 'i' starts at '5' and is only increased with '+=1' so 'i' will always be greater then 3


***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i < 9) {
i += 1
print (i)
}


```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift

var i = 5

while (i < 1000) {
i += 1
print (i)
}

```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
for i in 5...1000 where i % 2==0 {
print (i)
}

```

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
print("i = \(i)")
i += 1
}

//loop two
var i = 1

repeat {
print("i = \(i)")
i += 1
} while i <= 10
```
loop one is a 'while' statement but loop two is a 'repeat while' statement.  the code in loop one will check to see if 'i is less than 11' before adding 1 to the value of 'i'  the code in loop two will add 1 to the value of 'i'

***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.


a break statment is used as the default option in a switch statement and its action allows the code to continue executing below the switch statement.

a contine statement tells the code to go back to the begining of a loop as soon as a 'true' value is found and has the code to run the loop again on its next iteration 

***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
if (i >= 4 && i <= 7){
continue
}
print(i)
}
```
the code will only reach the "print" command when the "if" statement proves to be false (when i= 1,2,3,8,9,10). when the if statement proves to be true (when i= 4,5,6,7) the "continue" command forces the code to continue the loop and go back through the "if" statement

[]1
[]2
[]3
[]8
[]9
[]10

***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
if (i >= 4 && i <= 7){
break
}
print(i)
}
```
Code will print 1,2,3 because the 'break' moves the code out of the loop and down to the print function once for make the statment true.

[]1
[]2
[]3
[

***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
innerloop: for y in 1...3 {
if y == 2{
continue outerloop
}
print("x = \(x), y = \(y)")
}
}
```

the code will start with the lowest int from the inner loop and outter loops '1', printing those values.
then the code will start with the lowest int from the inner loop '1' and then the NEXT int from the outter loop '2', printing those values.
then the code will start with the lowest int from the inner loop '1' and then the FINAL int from the outter loop '3', printing those values.
since the code has moved through each of each of the possibilities of matching using '1' as the inner loop value it runs moves to the next value '2' which will start with the lowest int from the inner loop '1' and then the FINAL int from the outter loop '3', printing those values.


***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.


for x in 0...10 {
for y in 0...10 {
print("x = \(x), y = \(y)")
}


***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25
```

***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

var q23 = 4
for _ in 1...q23 {
for _ in 1...q23 {
print("* ", terminator: "")
}
print("")
}

***
