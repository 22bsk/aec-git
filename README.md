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

