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
