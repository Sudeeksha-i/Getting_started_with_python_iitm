# Print Statements

```print()``` is the simplest command and shows us output in console
```python
print("Hello World")
```

We can have have various strings in same ```print()```
```python
print("Hello", "Hi", "Namaste")
```

Not just strings we can also include numbers and decimals too
```python
print(10, 20.5, "Hi")
```

# Input Statements and Variables
```python
print("Enter a number: ")
```

```input()``` is used to get input from the user
```python
n=int(input()) 
```

```n``` is variable and is used in mathematical operations
```python
print(n)
print(n+1)
print(n+2)
```

# Variables and Litrals
Name is string (```str```)
```python
print("Enter your name: ")
s = str(input()) 
```

Number is integer (```int```)
```python
print("Enter a number: ")
n = int(input()) 
```

Fractional number is floating number (```float```)
```python
print("Enter a fractional number: ")
f = float(input())
```

Example to use all variables from above
```python
print("Hi", s, "your entered number", n, "and", f)
```

Merging ```input()``` statement with ```print()``` statement like below gives same result
```python
ss = str(input("Enter your name: "))
nn = int(input("Enter a number: "))
ff = float(input("Enter a fractional number: "))
print("Hi",ss,"your entered number",nn,"and",ff)
```

Change of variable mid-code
```python
ff = 52 #here "ff" is variable and "52" in literal 
print("Your ff variable in now changed to",ff)
ff=ff+1
print("Your ff variable in now changed to",ff)
```

Example
```python
r = int(input("Enter the Radius of the Circle: "))
area = 3.14*r*r
#here '3.14' is literal and 'r' is variable as '3.14' remains same for all iterations whereas 'r' changes
print("Area of the Entered Circle is", area)
```

# Data Types
```python
n=10 #it is an integer
print(n)

f = 6.3 #it is a decimal number
print(f)

s = "IITMOD" #it is a string 
print(s)
```

```type(x)``` tells class of ```x```
```python
print(type(n))

print("n is of type:",type(n))
print("f is of type:",type(f)) #float is a floating number i.e. Number other than interger
print("s is of type:",type(s))
```

```python
l = [10,20,30]
print(l) #displays all l
print(l[0]) #displays 1st element of l
print(l[1]) #displays 2nd element of l
print(l[2]) #displays 3rd element of l
#Note: Computer starts counting from 0
```

```l``` is of class ```list```
```python
print(type(l))
print(type(l[1])) #l[1] is of class 'int'
```

# Data Types continued

*Use ```print(x, type(x))``` to check the value and datatype of x*

```bool``` has only 2 values ```True``` and ```False```
```python
b1 = True #class of b1 datatype is 'bool'(Boolean)
b2 = False
```
Datatype Conversions in python with examples
```python
a = int(5.7) #here 5.7 is converted to int by dropping '.7' thus reulting to "5"
#Note : It does not round off. It just drops the decimal part
b = int("10") #here the str '10' is converted to int "10"

c = float(9) #this converts int '9' to float "9.0"
d = float("5.7") #this converts str '5.7'to int "5.7"

#the numbers are converted to str with same face value
e = str(9)
f = str(5.7)

g = bool(10) #bool value in 'True'
h = bool(0) #bool value in 'False'
i = bool(-10) #bool value in 'False'
#'0' is the only value with bool value "False"
#This observation is also vaild for float datatype

j = bool("IITM") #bool value in 'True'
k = bool("10.4") #bool value in 'True'
l = bool("-10") #bool value in 'True'
m = bool("0") #str '0' gives the bool value of 'True'

#bool has value of 'True' for all str except empty str
n = bool("") #bool value in 'False'
```

# Operators and Expressions
```python
n = 3*2
print(n) #prints '6'

a = 1
b = 2
c = a+b
print(c) #prints '3'

d = "IIT"
e = "Madras"

f = d*e #does not exist as sritng can not be multiplied
#Displays error "TypeError: can't multiply sequence by non-int of type 'str'"

g = d+e
print(g) #prints 'IITMadras'. This is called concatenation of str

h = [1,2,3]
i = [3,4,5]
j = h+i
print(j) #prints '[1,2,3,3,4,5]'. Puts all elements from both variables in one

k=10+13*2
print(k) #prints '36'. It is due to "operator precedence" i.e. it follows BODMAS.

l = 13
m = 7
o = l/m
print(o) #o is float inspite l and m being int
```
# Operators and Expressions continued

Arithimetic Operators ```(+, -, *, /, //, %, **)```
```python
a = 3
b = 2

print("Addition", a + b) #result = 5
print("Substraction", a - b) #result = 1
print("Multiplication", a * b) #result = 6
print("Division", a / b) #result = 1.5

print("Floor Division", a // b) #result = 1
#gives int(a/b) i.e. Quotient

print("Modulus", a % b) #result = 1
#gives the reminder

print("Exponential", a ** b) #result = 9
# gives the value of a power b.  i.e a^b
```

Relational Operators ```(>, <, >=, <=, ==, !=)```

*Relational operators always give ```bool``` value*
```python
print("Greater than", 5 > 10) #result = False
print("Greater than", 10 > 5) #result = True

print("Lesser than", 5 < 10) #result = True
print("Lesser than", 10 < 5) #result = False

print("Greater than", 5 > 5) #result = False
print("Greater than or Equal to", 5 >= 5) #result = True
print("Greater than or Equal to", 10 >= 5) #result = True

print("Lesser than", 5 < 5) #result = False
print("Lesser than or Equal to", 5 <= 5) #result = True
print("Lesser than or Equal to", 5 <= 10) #result = True

print("Equal to", 5 == 5) #result = True
print("Equal to", 5 ==50) #result = False

print("Not equal to", 5 != 5) #result = False
print("Not equal to", 5 != 50) #result = True
```

Logical Operatiors ```(and, or, not)```


```and``` = ' * ' ```(1*1=1, 1*0=0, 0*1=0, 0*0=0)```

```python
print(True and True) #result = True
print(True and False) #result = False
print(False and True) #result = False
print(False and False) #result = False
```

```or``` = ' + ' ```(1+1=1, 1+0=1, 0+1=1, 0+0=0)```
```python
print(True or True) #result = True
print(True or False) #result = True
print(False or True) #result = True
print(False or False) #result = False
```

```not``` = inverse
```python
print(not(True)) #result = False
print(not False) #result = True #the '()' is not mandatory
```

# Introduction to Strings
```python
s = "Coffee"
t = "Bread"

print(s)
print(t)
print(s+t) #it will concatenate

print(s[0]) #prints 1st letter
print(s[1]) #prints 2nd letter

print(s-t) #does not work/exist
```
String Slicing
```python
print(s[1:3]) #prints letters from 2nd to 3rd i.e. 'of'
print(s[1:5]) #prints letters form 2nd to 5th i.e. 'offe'
print(s[3:5]) #prints letters form 4th to 5th i.e. 'fe'
#This is called String Slicing
```
Indexing
```python
z = '0123456789'
a = z[4] #this is called 'Indexing'
b = z[7]
print(a) #prints 4
print(b) #prints 7
print(a+b) #prints 47. Does not print 11 as 'a' and 'b' are one letter strings.
c = int(a)
d = int(b)
print(c+d) #prints 11 after changing datatype
```
Example
```python
e = z[3]
f = z[8]
g = int(e+f)
h = ((int(e)) + (int(f)))
print(g) #prints 38
print(h) #prints 11
```

# More on Strings
Concatenation
```python
s = "Good"
print(s*5) #prints 'Good' 5 times in catenation
print(s[0]*5) #prints 'G' 5 times
```
```str``` comparison
```python
print(s == "Good") #Result = True
print(s =="good") #Result = False

print('apple' > 'one') #Result = False
print('four' < 'ten') #Result = True
#Here computer compares strings letter by letter
# It takes the 0th letter of 'apple' and 0th letter of 'one' i.e. 'a' and 'o' and compares then in alphabetical order.
# As 'a' come before 'o' in the order 'apple' is lesser than 'one' in string comparison
#Similarlly as 'f' come before 't', 'four' is lesser than 'ten' 

print("applea" > "appleb") #Result = False
#it compares all charecters if starting chatecters are same

print("abcde" > "abcdef") #Result = False
#After abcde, computer compares 'f' with 'None' and as f can't be less than 'None' value comes as false
```

Example of indexing
```python
a = 'python'
```
Indexing
```python
print(a[0]) #prints p
print(a[1]) #prints y
print(a[2]) #prints t
print(a[3]) #prints h
print(a[4]) #prints o
print(a[5]) #prints n
```
Negative Indexing
```python
print(a[-1]) #prints n
print(a[-2]) #prints o
print(a[-3]) #prints h
print(a[-4]) #prints t
print(a[-5]) #prints y
print(a[-6]) #prints p
```
```python
b = 'ancawoqhmxwrhfdacvribvyreaugiafcwniamghia'
print(b[100]) #shows error "IndexError: string index out of range" as 100 letter not there
```
```len(x)``` displays the length of variable ```x```
```python
print(len(b)) #prints total number of letters in b i.e 41

print(b[40]) #It is the last valid "Index" as python starts to count from 0 i.e 41-1 = 40 is the last letter
```

# PPA

PPA 1:
Print the first 5 positive integers in ascending order with one number in each line
```python
print(1)
print(2)
print(3)
print(4)
print(5)
```
PPA 2:
Print the following pattern.
```
*
**
***
****
*****
```
There are no spaces between consecutive stars. There are no spaces at the end of each line.
```python
print('*')
print('**')
print('***')
print('****')
print('*****')
```
PPA 3:
Accept an integer as input and print its square as output.
```python
n = int(input())
print(n*n)
```
PPA 4:
Accept two integers as input and print their sum as output.
```python
m = int(input())
n = int(input())
print(m+n)
```
PPA 5:
Accept two words as input and print the two words after adding a space between them.
```python
m = input()
n = input()
print(m,n)
```
PPA 6:
Accept the registration number of a vehicle as input and print its state-code as output.
```python
n = str(input())
print(n[0:2])
```
PPA 7:
Accept a five digit number as input and print the sum of its digits as output.
```python
n = input()
a = int(n[0])
b = int(n[1])
c = int(n[2])
d = int(n[3])
e = int(n[4])
print(a+b+c+d+e)
```

# GrPA

GrPA 1:
Accept five words as input and print the sentence formed by these words after adding a space between consecutive words and a full stop at the end.
```python
a = input()
b = input()
c = input()
d = input()
e = input()
print(f'{a} {b} {c} {d} {e}.')
```
GrPA 2:
Accept the date in DD-MM-YYYY format as input and print the year as output.
```python
n = str(input())
print(n[-4:])
```
GrPA 3:
Accept a sequence of five single digit numbers separated by commas as input. Print the product of all five numbers.
```python
n = str(input())
a = int(n[0])
b = int(n[2])
c = int(n[4])
d = int(n[6])
e = int(n[8])
print(a*b*c*d*e)
```
GrPA 4:
Assume that several IITs start offering online degrees across multiple branches. The email-id of a student is defined as follows:
```branch_degree_year_roll@student.onlinedegree.institute.ac.in```

For example, if the email-id is ```CS_BT_21_7412@student.onlinedegree.iitm.ac.in```, then this student is from the computer science branch, pursuing a BTech degree from IITM, starting from the year 2021, with 7412 as the roll number.

branch, degree and year are codes of length two, while roll and  institute are codes of length four. Accept a student's email-id as input and print the following details, one item on each line:

(1) Branch

(2) Degree

(3) Year

(4) Roll number

(5) Institute
```python
n = input()
branch = n[0:2]
degree = n[3:5]
year = n[6:8]
roll = n[9:13]
inst = n[-10:-6]
print(branch)
print(degree)
print(year)
print(roll)
print(inst)
```
GrPA 5:
Accept two positive integers x and y as input. Print the number of digits in x^y. You should be able to solve this problem using the concepts covered in week-1.
```python
m = int(input())
n = int(input())
o = str(m**n)
print(len(o))
```
GrPA 6:
Accept two positive integers M and N as input. There are two cases to consider:

(1) If M < N, then print M as output.

(2) If M >= N, subtract N from M. Call the difference M1. If M1 >= N, then subtract N from M1 and call the difference M2. Keep doing this operation until you reach a value k, such that, Mk <  N. You have to print the value of Mk as output. 

You should be able to solve this problem using the concepts covered in week-1.
```python
M = int(input())
N = int(input())
if (M < N):
   print(M)
elif (M >= N):
o = M % N
   print(o)
```
