# aec-git


# Sample text
text = "Hello, my email is example@example.com and my phone number is 123-456-7890."

# Define patterns
email_pattern = 'example@example.com'
phone_pattern = '123-456-7890'

# Find email addresses in the text
if email_pattern in text:
    print("Email found:", email_pattern)
else:
    print("Email not found")

# Find phone numbers in the text
if phone_pattern in text:
    print("Phone number found:", phone_pattern)
else:
    print("Phone number not found")
    ================
    # Python3 code to demonstrate working of
# Get matching substrings in string

# initializing string
test_str = "GfG is good website"

# initializing potential substrings
test_list = ["GfG", "site", "CS", "Geeks", "Tutorial" ]

# printing original string
print("The original string is : " + test_str)

# printing potential strings list
print("The original list is : " + str(test_list))


# Get matching substrings in string
res=[]
for i in test_list:
	if(test_str.find(i)!=-1 and i not in res):
		res.append(i)
# printing result
print("The list of found substrings : " + str(res))
=======================================================

  def add_matrices(matrix1, matrix2):
    if len(matrix1) != len(matrix2) or len(matrix1[0]) != len(matrix2[0]):
        raise ValueError("Matrices must have the same dimensions for addition.")
    
    result = []
    for i in range(len(matrix1)):
        row = []
        for j in range(len(matrix1[0])):
            row.append(matrix1[i][j] + matrix2[i][j])
        result.append(row)
    
    return result

# Example matrices
matrix1 = [[1, 2, 3],
           [4, 5, 6],
           [7, 8, 9]]

matrix2 = [[9, 8, 7],
           [6, 5, 4],
           [3, 2, 1]]

# Add matrices
result_matrix = add_matrices(matrix1, matrix2)

# Print result
for row in result_matrix:
    print(row)
=========================
# Program to add two matrices using nested loop
X = [[1, 2, 3],[4, 5, 6], [7, 8, 9]]
Y = [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

result = [[0, 0, 0], [0, 0, 0], [0, 0, 0]]

# iterate through rows
for row in range(len(X)):

	# iterate through columns
	for column in range(len(X[0])):
		result[row][column] = X[row][column]+ Y[row][column]

for r in result:
	print(r)
========================================
Add_result = [[X[row][column] + Y[row][column]
			for column in range(len(X[0]))] 
			for row in range(len(X))]
Sub_result = [[X[row][column] - Y[row][column]
			for column in range(len(X[0]))] 
			for row in range(len(X))]

print("Matrix Addition")
for r in Add_result:
	print(r)

print("\nMatrix Subtraction")
for r in Sub_result:
	print(r)
=========================
rmatrix = [[0, 0, 0], [0, 0, 0], [0, 0, 0]]

for row in range(len(X)):
	for column in range(len(X[0])):
		rmatrix[row][column] = X[row][column] * Y[row][column]
		
print("Matrix Multiplication",)
for r in rmatrix:
	print(r)
		
for i in range(len(X)):
	for j in range(len(X[0])):
		rmatrix[row][column] = X[row][column] // Y[row][column]

print("\nMatrix Division",) 
for r in rmatrix:
	print(r)
---------------------
X = [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

result = [[0, 0, 0], [0, 0, 0], [0, 0, 0]]

# iterate through rows
for row in range(len(X)):
	# iterate through columns
	for column in range(len(X[0])):
		result[column][row] = X[row][column]

for r in result:
	print(r)
	
# # Python Program to Transpose a Matrix using the list comprehension

# rez = [[X[column][row] for column in range(len(X))] 
# for row in range(len(X[0]))]

# for row in rez:
#	 print(row)
rrrrrrrrrrrrrrrr
Open In App

GEEKSFORGEEKS
Programs for printing pyramid patterns in Python
Exploring and creating pyramid patterns in Python is an excellent way to enhance your programming skills and gain a deeper understanding of loops and control structures. By modifying and experimenting with the provided examples, you can create a variety of captivating patterns using Python.

Exploring Pyramid Patterns in Python
Pyramid patterns are sequences of characters or numbers arranged in a way that resembles a pyramid, with each level having one more element than the level above. These patterns are often used for aesthetic purposes and in educational contexts to enhance programming skills.

Full Pyramid Patterns in Python
Full Pyramid Patterns in Python using Loop
Full Pyramid Patterns in Python Recursion
Pyramid Patterns in Python with Alphabet
Pyramid Patterns in Python with Number
Inverted Full Pyramid Patterns in Python
Hollow Pyramid Patterns in Python
Half Pyramid Patterns in Python
Half Pyramid Patterns in Python using Loop
Half Pyramid Patterns in Python using Recursion
Pyramid Patterns in Python with Numbers
Pyramid Patterns in Python with Alphabet
Inverted Pyramid Patterns in Python
Hollow Inverted Half Pyramid in Python
Full Pyramid Patterns in Python
A full pyramid pattern is a series of lines that form a pyramid-like structure. Each line contains a specific number of characters, and the number of characters on each line increases symmetrically as we move down the pyramid.

Example 1: Full Pyramid Patterns in Python using Loop

# Function to print full pyramid pattern

def full_pyramid(n):

    for i in range(1, n + 1):

        # Print leading spaces

        for j in range(n - i):

            print(" ", end="")

         

        # Print asterisks for the current row

        for k in range(1, 2*i):

            print("*", end="")

        
Output

    *
   ***
  *****
 *******
*********

Example 2: Full Pyramid Patterns in Python Recursion


def print_space(space):

    if space > 0:

        print(" ", end="")

        print_space(space - 1)
 

def print_star(star):

    if star > 0:

        print("* ", end="")

        print_star(star - 1)
 

def print_pyramid(n, current_row=1):

    if current_row > n:

        return
 

    spaces = n - current_row

    stars = 2 * current_row - 1
 

    # Print spaces

    print_space(spaces)
 

    # Print stars

    print_star(stars)
 

    # Move to the next line for the next row

    print()
 

    # Print the pyramid for the next row

    print_pyramid(n, current_row + 1)
 
# Set the number of rows for the pyramid

n = 5
 
# Print the pyramid pattern
print_pyramid(n)
Output

    * 
   * * 
  * * * 
 * * * * 
* * * * * 

Example 3: Pyramid Patterns in Python with Alphabet


n = 5

alph = 65

for i in range(0, n):

    print(" " * (n-i), end=" ")

    for j in range(0, i+1):

        print(chr(alph), end=" ")

        alph += 1

    alph = 65

    print()
Output

      A 
     A B 
    A B C 
   A B C D 
  A B C D E 

Example 4: Pyramid Patterns in Python with Number


def print_number_pyramid(rows):

    for i in range(1, rows + 1):

        # Print spaces

        for j in range(rows - i):

            print(" ", end="")

        # Print numbers

        for j in range(2 * i - 1):

            print(j + 1, end="")

        # Move to the next line after each row

        print()
 
# Example usage

num_rows = 5
print_number_pyramid(num_rows)
Example 5: Inverted Full Pyramid Patterns in Python

# Function to print inverted full pyramid pattern

def inverted_full_pyramid(n):

    # Outer loop for the number of rows

    for i in range(n, 0, -1):

        # Inner loop for leading spaces in each row

        for j in range(n - i):

            print(" ", end="")

        # Inner loop for printing asterisks in each row

        for k in range(2*i - 1):

            print("*", end="")

        # Move to the next line after each row

        print("\r")
 
# Set the value of n (number of rows)

n = 5
 
# Call the function to print the inverted full pyramid
inverted_full_pyramid(n)
Output

*********
 *******
  *****
   ***
    *

Example 6: Hollow Pyramid Patterns in Python


def hollow_pyramid(n):

    for i in range(1, n + 1):

        for j in range(1, 2 * n):

            if j <= n - i or j >= n + i:

                print(" ", end="")

            else:

                print("*", end="")

        print()
 
# Set the number of rows for the pyramid

rows = 5
 
# Call the function with the specified number of rows
hollow_pyramid(rows)
Output

      *    
   *     *   
  *       *  
 *          * 
*********

Half Pyramid Patterns in Python
In this example, the half pyramid starts with one asterisk in the first row and adds one more asterisk in each subsequent row. The print(“\r”) statement is used to move to the next line after printing each row. You can customize the value of n to create a half pyramid with a different number of rows.

Example 1: Half Pyramid Patterns in Python using Loop

# Function to print a half pyramid pattern

def half_pyramid(n):

    for i in range(1, n + 1):

        for j in range(1, i + 1):

            print("* ", end="")

        print("\r")
 
# Example: Print a half pyramid with 5 rows

n = 5
half_pyramid(n)
Output

* 
* * 
* * * 
* * * * 
* * * * * 

Example 2: Half Pyramid Patterns in Python using Recursion


def print_half_pyramid(n):

    if n > 0:

        # Call the function recursively with a smaller value of n

        print_half_pyramid(n - 1)

         

        # Print '*' characters for the current row

        print('*' * n)
 
# Get the number of rows from the user

rows = int(input("Enter the number of rows for the half pyramid: "))
 
# Call the function to print the half pyramid pattern
print_half_pyramid(rows)
Output

*
**
***
****
*****
Example 3: Pyramid Patterns in Python with Numbers

# Function to demonstrate printing pattern of numbers

def numpat(n):

     

    # initialising starting number 

    num = 1
 

    # outer loop to handle number of rows

    for i in range(0, n):

     

        # re assigning num

        num = 1

     

        # inner loop to handle number of columns

            # values changing acc. to outer loop

        for j in range(0, i+1):

         

                # printing number

            print(num, end=" ")

         

            # incrementing number at each column

            num = num + 1

     

        # ending line after each row

        print("\r")
 
# Driver code

n = 5
numpat(n)
Output

1 
2 3 
4 5 6 
7 8 9 10 
11 12 13 14 15 

Example 4: Half Pyramid Patterns in Python in Alphabets

# Function to demonstrate printing pattern of alphabets

def alphapat(n):

     

    # initializing value corresponding to 'A' ASCII value

    num = 65
 

    # outer loop to handle number of rows 5 in this case

    for i in range(0, n):

     

        # inner loop to handle number of columns

        # values changing acc. to outer loop

        for j in range(0, i+1):

         

            # explicitly converting to char

            ch = chr(num)

         

            # printing char value 

            print(ch, end=" ")

     

        # incrementing number

        num = num + 1

     

        # ending line after each row

        print("\r")
 
# Driver Code

n = 5
alphapat(n)
Output

A 
B B 
C C C 
D D D D 
E E E E E 

Example 5: Inverted Pyramid Patterns in Python

# Function to print inverted half pyramid pattern

def inverted_half_pyramid(n):

    for i in range(n, 0, -1):

        for j in range(1, i + 1):

            print("* ", end="")

        print("\r")
 
# Example: Inverted Half Pyramid with n = 5

n = 5
inverted_half_pyramid(n)
Output

* * * * *
* * * *
* * *
* *
*

Example 6: Hollow Inverted Half Pyramid in Python

In this modified version, an additional check is added inside the second inner loop to determine whether to print a ” or a space. The condition if j == 0 or j == i – 1 or i == rows: ensures that ” is printed at the beginning, end, and for the last row, while spaces are printed in between. Adjust the value of num_rows to change the size of the hollow inverted half pyramid.


def print_hollow_inverted_half_pyramid(rows):

    for i in range(rows, 0, -1):

        for j in range(rows - i):

            print(" ", end="")

        for j in range(i):

            if j == 0 or j == i - 1 or i == rows:

                print("*", end="")

            else:

                print(" ", end="")

        print()
 
# Example usage

num_rows = 5

print("Hollow Inverted Half Pyramid:")
print_hollow_inverted_half_pyramid(num_rows)
Output

Hollow Inverted Half Pyramid:
*****
*   *
*  *
* *
**


Article Tags : Python pattern-printingpythonPython Pattern-printing
Read Full Article
A-143, 9th Floor, Sovereign Corporate Tower, Sector-136, Noida, Uttar Pradesh - 201305
Company
About Us
Legal
Careers
In Media
Contact Us
Advertise with us
GFG Corporate Solution
Placement Training Program
Explore
Job-A-Thon Hiring Challenge
Hack-A-Thon
GfG Weekly Contest
Offline Classes (Delhi/NCR)
DSA in JAVA/C++
Master System Design
Master CP
GeeksforGeeks Videos
Geeks Community
Languages
Python
Java
C++
PHP
GoLang
SQL
R Language
Android Tutorial
DSA
Data Structures
Algorithms
DSA for Beginners
Basic DSA Problems
DSA Roadmap
DSA Interview Questions
Competitive Programming
Data Science & ML
Data Science With Python
Data Science For Beginner
Machine Learning Tutorial
ML Maths
Data Visualisation Tutorial
Pandas Tutorial
NumPy Tutorial
NLP Tutorial
Deep Learning Tutorial
Web Technologies
HTML
CSS
JavaScript
TypeScript
ReactJS
NextJS
NodeJs
Bootstrap
Tailwind CSS
Python Tutorial
Python Programming Examples
Django Tutorial
Python Projects
Python Tkinter
Web Scraping
OpenCV Tutorial
Python Interview Question
Computer Science
GATE CS Notes
Operating Systems
Computer Network
Database Management System
Software Engineering
Digital Logic Design
Engineering Maths
DevOps
Git
AWS
Docker
Kubernetes
Azure
GCP
DevOps Roadmap
System Design
High Level Design
Low Level Design
UML Diagrams
Interview Guide
Design Patterns
OOAD
System Design Bootcamp
Interview Questions
School Subjects
Mathematics
Physics
Chemistry
Biology
Social Science
English Grammar
Commerce
Accountancy
Business Studies
Economics
Management
HR Management
Finance
Income Tax
UPSC Study Material
Polity Notes
Geography Notes
History Notes
Science and Technology Notes
Economy Notes
Ethics Notes
Previous Year Papers
Preparation Corner
Company-Wise Recruitment Process
Resume Templates
Aptitude Preparation
Puzzles
Company-Wise Preparation
Companies
Colleges
Competitive Exams
JEE Advanced
UGC NET
SSC CGL
SBI PO
SBI Clerk
IBPS PO
IBPS Clerk
More Tutorials
Software Development
Software Testing
Product Management
Project Management
Linux
Excel
All Cheat Sheets
Free Online Tools
Typing Test
Image Editor
Code Formatters
Code Converters
Currency Converter
Random Number Generator
Random Password Generator
Write & Earn
Write an Article
Improve an Article
Pick Topics to Write
Share your Experiences
Internships
@GeeksforGeeks, Sanchhaya Education Private Limited, All rights reserved

