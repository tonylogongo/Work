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

----------- NEW CODE --------------

# Function to calculate hotel cost
def hotel_cost(num_nights):
    # Assuming a price per night of £100
    return num_nights * 100

# Function to calculate plane cost
def plane_cost(city_flight):
    # Assigning flight costs based on city
    if city_flight == "Spain":
        return 500
    elif city_flight == "Morroco":
        return 700
    elif city_flight == "Kenya":
        return 1000
    else:
        return 0  # 0 will be the default return value if city not found

# Function to calculate car rental cost
def car_rental(rental_days):
    # Daily rental cost of £50
    return rental_days * 70

# Function to calculate total holiday cost
def holiday_cost(num_nights, city_flight, rental_days):
    total_cost = hotel_cost(num_nights) + plane_cost(city_flight) + car_rental(rental_days)
    return total_cost

# Get user inputs
city_flight = input("Enter the city you will be flying to (Kenya, Spain or Morroco): ")
num_nights = int(input("Enter the number of nights you will be staying at a hotel: "))
rental_days = int(input("Enter the number of days for which you will be hiring a car: "))

# Calculate total holiday cost
total_cost = holiday_cost(num_nights, city_flight, rental_days)

# Print details about the holiday
print("\nHoliday Details:")
print(f"City of Flight: {city_flight}")
print(f"Number of Nights in Hotel: {num_nights}")
print(f"Number of Days for Car Rental: {rental_days}")
print(f"Total Holiday Cost: £{total_cost}")

--------- NEW CODE ----------

def linear_search(arr, target):
    """Performs linear search to find the target element in the array."""
    for i, num in enumerate(arr):
        if num == target:
            return i
    return -1

def insertion_sort(arr):
    """Sorts the array using the insertion sort algorithm."""
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key

# Given array
arr = [27, -3, 4, 5, 35, 2, 1, -40, 7, 18, 9, -1, 16, 100]

# Search for 9 using Linear Search
index = linear_search(arr, 9)
print("Index of 9 using Linear Search:", index)

# Sort the array using Insertion Sort
insertion_sort(arr)
print("Sorted array using Insertion Sort:", arr)

# Search for 9 in the sorted array using Binary Search
def binary_search(arr, target):
    """Performs binary search to find the target element in the sorted array."""
    low = 0
    high = len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    return -1

index_sorted = binary_search(arr, 9)
print("Index of 9 in the sorted array using Binary Search:", index_sorted)

---------- NEW CODE ---------

class Album:
    def __init__(self, album_name, number_of_songs, album_artist):
        self.album_name = album_name
        self.number_of_songs = number_of_songs
        self.album_artist = album_artist
    
    def __str__(self):
        return f"({self.album_name}, {self.album_artist}, {self.number_of_songs})"

# Creating a list of albums
albums = [
    Album("Positions", 17, "Ariana Grande"),
    Album("Thriller", 9, "Michael Jackson"),
    Album("After Hours", 10, "The Weeknd"),
    Album("The Dark Side of the Moon", 10, "Pink Floyd"),
    Album("Blond", 11, "Frank Ocean")
]

# Printing the original list of albums
print("Original list of albums:")
for album in albums:
    print(album)

# Sorting the list according to the number of songs
albums.sort(key=lambda x: x.number_of_songs)
print("\nSorted list of albums by number of songs:")
for album in albums:
    print(album)

# Swapping elements at positions 1 and 2
albums[1], albums[2] = albums[2], albums[1]
print("\nList of albums after swapping elements at positions 1 and 2:")
for album in albums:
    print(album)

# Creating a new list of albums
albums2 = [
    Album("Take Care", 5, "Drake"),
    Album("CTRL", 8, "Sza"),
    Album("A Night at the Opera", 12, "Queen"),
    Album("Mama's Gun", 13, "Erykah Badu"),
    Album("Training Day", 5, "Potter Payper")
]

# Copying albums from albums2 to albums
albums.extend(albums2)

# Adding two new albums
albums.append(Album("Dark Side of the Moon", 9, "Pink Floyd"))
albums.append(Album("Oops!... I Did It Again", 16, "Britney Spears"))

# Sorting albums alphabetically by album name
albums.sort(key=lambda x: x.album_name)
print("\nSorted list of albums alphabetically by album name:")
for album in albums:
    print(album)

# Searching for "Dark Side of the Moon" and printing its index
for i, album in enumerate(albums):
    if album.album_name == "Dark Side of the Moon":
        print("\nIndex of 'Dark Side of the Moon' in the list:", i)

-------- NEW CODE ---------

def adding_up_to(lst, index):
    if index == 0:
        return lst[0]
    else:
        return lst[index] + adding_up_to(lst, index - 1)

# Test cases
print(adding_up_to([1, 4, 5, 3, 12, 16], 4))  # Output: 25
print(adding_up_to([4, 3, 1, 5], 1))          # Output: 7
