# Import Library
import numpy as np  # NumPy library for numerical operations

# ------------------ 1D Array ------------------
# Create 1D array
arr = np.array([1,2,3,4,5,6])
print(arr)

# Print type
print(type(arr))  # <class 'numpy.ndarray'>

print("-------------------------------------------------------------------")

# ------------------ 2D Array ------------------
# Create 2D array
arr2 = np.array([
    [1,2,3],
    [4,5,6]
])
print(arr2)

# Shape (rows, columns)
print(arr2.shape)  # prints (2,3)

print("--------------------------------------------------------------")

# ------------------ Special Arrays ------------------
# Array of zeros
print(np.zeros((3,3)))  # 3x3 matrix of zeros

# Array of ones
print(np.ones((2,2)))   # 2x2 matrix of ones

# Range of numbers
print(np.arange(1,5))   # array from 1 to 4

print("----------------------------------------------------------")

# ------------------ Reshape ------------------
new = arr2.reshape((6,1))  # reshape 2x3 to 6x1
print(new)

print("----------------------------------------------------------")

# ------------------ Operations ------------------
a = np.array([1,2,3])
b = np.array([5,6,7])

print(a + b)  # addition
print(a - b)  # subtraction
print(a * b)  # element-wise multiplication
print(a / b)  # element-wise division

print(np.sum(a))  # sum of elements
print(a[1])       # access 2nd element

print("--------------------------------------------------------------")

# ------------------ Access & Slicing ------------------
# Access element
print(arr2[0,2])  # first row, third column

# Slicing
c = np.array([10,20,30,40,50,60])
print(c[0:3])  # first 3 elements
print(c[1:])   # from second element to end
print(c[:4])   # first 4 elements

print("-----------------------------------------------------------")

# Slicing in matrix
d = np.array([
    [1,2,3],
    [4,5,6],
    [7,8,9]
])
print(d[0])         # first row
print(d[:,0])       # first column
print(d[0:2 , 1:3]) # part of matrix (2x2 block)

print("---------------------------------------------------------------")

# ------------------ Editing Array ------------------
e = np.array([500,60,70,80,90])
e[3] = 100  # change 4th element to 100
print(e)

print("--------------------------------------------------------------")

# ------------------ Random Values ------------------
print(np.random.rand(5))      # 5 random floats between 0 and 1
print(np.random.rand(10,5))   # 10x5 matrix of random floats
print(np.random.randint(1,10,5))  # 5 random integers from 1 to 9

print("-----------------------------------------------------------------")

# ------------------ Statistics ------------------
w = np.array([8,9,6,7,5])
print(np.max(w))    # max value
print(np.min(w))    # min value
print(np.mean(w))   # mean
print(np.median(w)) # median
print(np.std(w))    # standard deviation

print("----------------------------------------------------------------------")

# ------------------ Filtering & Broadcasting ------------------
p = np.array([20,30,50,81])
print(p > 25)      # boolean mask
print(p[p > 25])   # filtered array

print(p + 5)       # broadcasting: add 5 to each element

print("--------------------------------------------------------------------")

# ------------------ Matrix Multiplication ------------------
o = np.array([[1,2],[5,8]])
u = np.array([[5,6],[10,6]])
print(np.dot(o,u))  # matrix multiplication

print("-----------------------------------------------------------------------")

# ------------------ Transpose & Flatten ------------------
r = np.array([[50,55,8,89],[60,90,70,66]])
print(r.T)          # transpose
print(r.flatten())  # flatten to 1D

print("-------------------------------------------------------------------------")

# ------------------ Save & Load Data ------------------
np.save("data.npy", r)      # save array to file
loaded = np.load("data.npy") # load array from file
print(loaded)

print("------------------------------------------------------------------------")

# ------------------ Unique Values ------------------
arr_unique = np.array([1,2,2,3,4,4,5])
print(np.unique(arr_unique))  # unique elements

print("------------------------------------------------------------------------")

# ------------------ Rounding Functions ------------------
arr22 = np.array([1.2, 2.6, 3.5, 4.1])
print(np.round(arr22))  # np.round: rounds each element to the nearest integer

arr33 = np.array([1.9, 2.3, 3.7, 4.1])
print(np.floor(arr33))  # np.floor: rounds each element down to the nearest integer (floor)

arr44 = np.array([1.2, 2.3, 3.8, 4.1])
print(np.ceil(arr44))   # np.ceil: rounds each element up to the nearest integer (ceiling)

arr55 = np.array([1.9, 2.3, 3.7, 4.1])
print(np.trunc(arr55))  # np.trunc: truncates the decimal part, keeping only the integer part
