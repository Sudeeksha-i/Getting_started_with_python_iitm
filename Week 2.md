# Variable: A Programmer's Perspective

A progammer should always try to make variable 'self-explainatory'

```#``` is used to comment. Comment is not run my the computer

```python
ram_bank_balance = 100000
#ram's bank balance, note this is his positive
ram_loan = 500000
#ram's load, this is to be returened by him and hence will count as negetive

lakshman_bank_balance = 2000000
#lakshman's bank balance, note this is his positive
lakshman_loan = 1000000
#lakshman's load, this is to be returened by him and hence will count as negetive

net_income = ram_bank_balance+lakshman_bank_balance
#net_income is total bank balance of the two brothers

net_liability = ram_loan+lakshman_loan
#net_liability is the total loan of the brothers

final_value = net_income-net_liability
#final_value is the family's final money (could be +ve or -ve)

print("The family has",final_value)
```
Using comments is a good programmer practice.

It makes everyone understand the code better.

# Variable Revisited: Dynamic Typing

We are trying to illustrate what we call the dynamic typing
```python
a = 10
print(type(a)) #prints type of a i.e. 'int'

a = "india"
print(type(a)) #prints type of a i.e. 'str'
# 'a' changes its type to the one it stores value of
```
This is called 'Dynamic Typing'

```type``` of a variable is dynamic in python
```python
n = 10
print(type(n)) #prints 'int'
print(n) #prints 10
n=n/2
print(type(n)) #prints 'float'
print(n) #prints 5.0 (float)
```
Note: python changes ```int``` to ```float``` on division even by 1
```python
m = 10
print(type(m)) #prints 'int'
print(m) #prints 10
m=m/2
print(type(m)) #prints 'float'
print(m) #prints 10.0 (float)
```

# More on Variable, Operators and Ecpressions

```if, else, while, for, and, or, not, as```, etc are called keywords defined by the python

Keywords can not be used as name of variables in python

example:
```python
and = s
print(and) 
```
The above code shows an error as ```SyntaxError: invalid syntax```

There are other rule for naming a variable. 

The first rule says, we can use only alphanumeric characters and underscore (```_```) in variable name.

Alphanumeric characters include all alphabets from A to Z in lowercase, as well as uppercase and all numbers from 0 to 9. Python supports only one special variable underscore ```_```

Example for valid variable names:
```python
A = 65 
a = 1
a1 = 213468
a_1 = 79
asdfdg = 8
adsf_dfgh = 85
asrt23456 = 53
oiFSf_9GF76_nFvc = 26
```

The second rule says; we must start a variable name with an alphabet or an underscore, but we cannot start it with a number.

Example:
```python
1a = 5 #it is invalid
a1 = 5 #it is valid
_1a = 5 #it is valid
```

The third rule says, is variable names are case sensitive.
```python
roll = 4
ROLL = 65
Roll = 156
print(roll,ROLL,Roll) #prints '4 65 156'
#varibles are case-sensitive inspite the spellings being the same
```

Example of invalid variable names:
```python
12fds = 265 #should not start with a number
dsa fsd = 4562 #should not have space in between
dfsa*fdsa = 456 #should not have special charecters
```

## Multiple assignment
```python
x,y = 10,20 
```
This is called multiple assignment
```python
print(x,y) #prints '10 20'
#python assings values respective to the place 
#i.e. x=10 as it is assgined first
#y = 20 as it is assigned second
```
NOTE: x,y is not a variable.

Here is 'x' and 'y' are separate variables.

```python
a = b = c = 10
print(a,b,c) #prints '10 10 10'
#this is a way to assing a value to multiple variables

m,n = o,p = 2,3
print(m,n,o,p) #prints '2 3 2 3'

q,r = 5,6
print(q,r) #prints '5 6'
q,r = r,q #this is simple swapping
print(q,r) #prints '6 5'
```

## Ways to 'Delete a Variable'
```python
t = 10
print(t) #prints '10'
del t #'del t' removes the variable 't'
print(t) #shows error "NameError: name 't' is not defined"
```
Note: del t can also be written as del(t)

## Shorthand operators

In common arthimetic we usually write increment as this
```python
count = 0
count = count + 1
count = count + 1
count = count + 1
count = count + 1
count = count + 1
print(count) #prints '5'
```
Using shorthand operators we can simplify this as
```python
count = 0
count +=1 #this is read as "count = count +1"
count +=1 #this short-hand operators makes programmers life easy
count +=1 #as generally we do many increments and decrements
count +=1
count +=1 #it helps us by saving our time
print(count) #prints '5' 
```
Here, We get the same result with less effort

More examples on shorthand:
```python
count = 10
count = count - 1
count -= 1
print(count) #prints '8'

count = count *2
count *= 2
print(count) #prints '32' i.e. 8*2*2

count = count/2
count /= 2
print(count) #prints '8.0' i.e (32/2)/2
```
## in-Operator

It allows us to perform a similar operation, which usually happens with search engines,where we type some keywords and that particular keyword, is checked against all the possible documents and if there is a match, then we get that document in the search results.
```python
print('alpha' in 'A variable name can only contain alpha numerical charecters and underscore') #prints 'True'
print('alpha' in 'A variable name must start with a letter or the underscore charecter') #prints 'False'
```
The in-operator checks, if a particular value exists in somethin else or not, which means a computer is actually checking a string alpha exists inside this particular string or not.

The result of in-operator is always Boolean ```bool``` value 

## Chaining Operators

When we use multiple relational operators in the single statement, then it is called as chaining operators.
```python
x = 5
print(1 < x < 10) #prints 'True'
print(10 < x < 20) #prints 'False'
print(x < 10 < x*10 <100) #print 'True'
print(10 > x <=9) #prints 'True'
print(5 == x > 4) #prints 'True'
```
NOTE: every statement is to be satisfied to be 'True'

# Escape characters and types of quotes

## Escape Characters
```python
print('It's a beautiful day') #shows "SyntaxError: invalid syntax"
```
Computer doesn't diffrentiate between the 's and ''(single quotes) which are usually used in writing print statments

It considers 'It' as a string and '')' as another string

Solution for such errors:
```python
print("It's a beautiful day") #using double quotes
```
or using a escape charecter
```python
print('It\'s a beautiful day') #using backslash( \ ) 
```
This charecter ```\``` is refered as 'Escape Charecter'
```python
print("We are from "IIT" Madras) #shows "SyntaxError: invalid syntax"
```
Here computer thinks ```We are from``` and ``` Madras``` as strings leaving IIT
```python
print("We are from \"IIT\" Madras") #using ecsape charecter we can fix this
```
```python
print("I am the author of this page. I am using markdown format") #prints are usually
```
But if we want to add extra space after the full stop we can use escape charecter like displayed below
```python
code:
  print("I am the author of this page.\t I am using markdown format") #prints with space after fullstop
```
```
output:
  I am the author of this page.    I am using markdown format
```
```python
code:
  print("I am the author of this page.\n I am using markdown format") #prints 'I am using markdown format' in next line
```
```
output:
  I am the author of this page.
  I am using markdown format
```

## Use of Quotes supported by python
```python
x = "this is a string"
y = "this is also a string"
print(x) #prints as usual
print(y)
```
```python
z ="first line
second line
third line"
print(z)
```
It shows an error saying ```SyntaxError: EOL while scanning string literal```
Where'EOL' == End Of the Line
Here Computers keeps on searching the the quote to end in the same line
A string is stored in single line
```python
a = '''First Line
Second Line
Third Line'''
print(a) #prints all three line usually
# 3' are used to store multiple line strings
```
```python
'''
triple qutoes can also be used for commenting as '#' to store mulitiple lines as '#' is only a single line comment
'''
```

# String Methods

Screenshots to be uploaded....

# An Intresting Cipher: More on Strings
```python
alpha = 'abcdefghijklmnopqrstuvwxyz'
print(alpha[0]) #prints 'a'

i = 0
print(alpha[i]) #prints 'a'
print(alpha[i+1]) #prints 'b'
print(alpha[i+2]) #prints 'c'
print(alpha[i+3]) #prints 'd'

i = 10
print(alpha[i]) #prints 'k'
print(alpha[i+1]) #prints 'l'
print(alpha[i+2]) #prints 'm'
print(alpha[i+3]) #prints 'n'


i = 20
print(alpha[i]) #prints 'u'
print(alpha[i+1]) #prints 'v'
print(alpha[i+2]) #prints 'w'
print(alpha[i+3]) #prints 'x'


i = 25
print(alpha[i]) #prints 'k'
print(alpha[i+1]) #shows error 'IndexError: string index out of range'
print(alpha[i+2]) #as max len of alpha is 25
print(alpha[i+3])

print(alpha[20]) #prints 'u'

i = 30
print(alpha[i%26]) #prints 'e' 
#i.e reminder of 30 devided 26 which is 4 ==e
print(alpha[4]) #prints 'e'

i = 26
print(alpha[i%26]) #prints 'a'

i=24
print(alpha[i]) #prints 'y'
print(alpha[i+1]) #prints 'z'
print(alpha[i+2]) #shows error 'IndexError: string index out of range'

print(alpha[i]%26) #prints 'y'
print(alpha[i+1]%26) #prints 'z'
print(alpha[i+2]%26) #print 'a'

#i%26 is rotating in index of alpha

s = 'python'
#We expect to output qzuipo
#we need the next letter of the string s

t = ""

print(alpha.index(s[0])) #prints '15' 
#i.e index of P in alpha

t=t+(alpha[((alpha.index(s[0]))+1)%26]) #checks the next alpha by increasing the indexing 
print(t) #print 'q'

t=t+(alpha[((alpha.index(s[1]))+1)%26]) #t+(alpha.....) means concatenate previous value of 't' with new letter obtained
print(t) #prints 'qz'

#similarly
t=t+(alpha[((alpha.index(s[2]))+1)%26])
t=t+(alpha[((alpha.index(s[3]))+1)%26])
t=t+(alpha[((alpha.index(s[4]))+1)%26])
t=t+(alpha[((alpha.index(s[5]))+1)%26])
print(t) #prints 'qzuipo'
#Hence expected outcome is achevied with this code using the concepts learnet in this Chapter

t = ''

#example use of variables
t = ''
i=0
k=1
t=t+(alpha[((alpha.index(s[i]))+k)%26])
t=t+(alpha[((alpha.index(s[i+1]))+k)%26])
t=t+(alpha[((alpha.index(s[i+2]))+k)%26])
t=t+(alpha[((alpha.index(s[i+3]))+k)%26])
t=t+(alpha[((alpha.index(s[i+4]))+k)%26])
t=t+(alpha[((alpha.index(s[i+5]))+k)%26])
print(t) #prints same result like before code

#to shift the 's' 2 letters we can use the same code and simply cangeing the value of 'k' to 2

t = ''
i=0
k=2
t=t+(alpha[((alpha.index(s[i]))+k)%26])
t=t+(alpha[((alpha.index(s[i+1]))+k)%26])
t=t+(alpha[((alpha.index(s[i+2]))+k)%26])
t=t+(alpha[((alpha.index(s[i+3]))+k)%26])
t=t+(alpha[((alpha.index(s[i+4]))+k)%26])
t=t+(alpha[((alpha.index(s[i+5]))+k)%26])
print(t) #prints 'ravjqp' i.e 's' shifted by 2 letters

#we can use the same same code for multiple shifting by just changing the value of 'k'
t = ''
i=0
k=3
t=t+(alpha[((alpha.index(s[i]))+k)%26])
t=t+(alpha[((alpha.index(s[i+1]))+k)%26])
t=t+(alpha[((alpha.index(s[i+2]))+k)%26])
t=t+(alpha[((alpha.index(s[i+3]))+k)%26])
t=t+(alpha[((alpha.index(s[i+4]))+k)%26])
t=t+(alpha[((alpha.index(s[i+5]))+k)%26])
print(t) #prints 'sbwkrq'
```
This is popularly called Ceasar Cipher in cryptography

# Introduction to the if statement

## if condition
Let us consider movie "Avengers". This is a 13+ movie.
```python
print("Please enter your date of birth")
birth_year = int(input())

current_year = 2021

age = current_year-birth_year

if (age<13):
  print("You are under age, you cannot watch this movie.")
  print("Wait untill you are old enough to watch this moive.")
else:
  print("You are old enough to watch Avengers, Enjoy!")
  print("Dont forget to watch sequels and prequels")
  
print("Have a Nice time!") #this part excecutes no matter if 'if-statment' was satisfied or not
```
