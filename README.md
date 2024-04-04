# Codes I have wrote
These are some codes that I have written since I began learning!

# This code was based on basic understanding of numbers and storing them as integers
a = input("Enter any 2 digit number:")
b = input("Enter any 2 digit number:")
c = input("Enter any 2 digit number:")
a =  int (a)        # This'll store the users input as an integer
b =  int (b)        # This'll store the users input as an integer
c =  int (c)        # This'll store the users input as an integer

# This will minus the users 1st number by the 2nd number
sum1 = a - b 

# This'll multiply the last number by the 1st number
sum2 = c*a          

# Adds together all 3 numbers and then divide that number by the last number they gave
sum3 = a + b + c/c  

print(sum1)         
print(sum2)         
print(sum3)         

----------- NEW CODE ---------------

# This is demonstaring a bit more of a deeper knowledge into numbers in python but still quite basic

# REMEMBER!! The first character is index 0 not index 1!! Example: "radio" - r = index 0 & a would be index 1

# math.floor() = round down
# math.celi() = round up
# math.trunc() = Cuts off the decimal part of the float

import math 

name = "Tony Logongo"

# This would print starting from index 1 and finsing but not including index 3 
print(name[1:3])        

 # This would print how many characters are in the string. len standing for LENGTH
print(len(name))       

# This will print off everty 4th letter with index 1 being the starting point
print(name[1::4])       

# This would start at index 3 going backwards to index 0. However the (-1) means that once it reaches index 0 it will skip back one space to index 1. Meaning the output would be 'yno'
print(name[3:0:-1])  

num1 = 10
num2 = 93.5905934
# Converts number from integer to a float
print(float(num1)) 

# Converts number from float to integer
print(int(num2))        

# This'll round 'num2' to the nearest whole number
print(round(num2)) 

# This'll round 'num2' to 2 decimal points
print(round(num2,2)) 
   
-------------- NEW CODE --------------

# This is me trying to manipulate the user's input
sentence = input("Write me any sentence of your choice")

# This will store the user's answers
str_mani = sentence         

# This'll use the data recieved from 'str_mani' to find the length of that data
print(len(str_mani))        

# This'll store whatever the last letter of the sentence is
char1 = sentence [-1]       

# This'll print the last 3 letters of the sentence bsckwards 
print(str_mani[-1:-4:-1])   

# This'll replace whatever the last letter is by the @ symbol
print(str_mani.replace(char1, " @")) 
print(str_mani[0:3])

# This'll print the first 2 characters of the sentence and the last 2 characters of the sentece put together
print(str_mani[0:3] + str_mani[-2:]) 

------------- NEW CODE ------------ 

# Learning Lists

# Indexing the list and changing the information
pets[3] = "Tony"
print(pets[3])

# Adding to the list 
pets.append("Cow")
print(pets)

# Deleting an item from the list
del pets[6]
print(pets)

num_lists = ["1", "4", "4", "8", "6", "5", "3"]

# Casting each element in "num_list" to an integer
num_int = [int(element) for element in num_lists] 

# Taking the intgers and multiplying everything inside by 2
total = sum(num_int * 2)

print(total)
