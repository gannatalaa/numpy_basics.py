# Import Library
import numpy as np

# Create 1D array
arr = np.array([1,2,3,4,5,6])
print(arr)

# Print type
print(type(arr))

print("-------------------------------------------------------------------")

# Create 2D array
arr2 = np.array([
    [1,2,3],
    [4,5,6]
])

print(arr2)

# Shape (rows , columns)
print(arr2.shape)

print("--------------------------------------------------------------")

# Array of zeros
print(np.zeros((3,3)))

# Array of ones
print(np.ones((2,2)))

# Range of numbers
print(np.arange(1,5))

print("----------------------------------------------------------")

# Reshape
new = arr2.reshape((6,1))
print(new)

print("----------------------------------------------------------")

# Operations
a = np.array([1,2,3])
b = np.array([5,6,7])

print(a + b)
print(a - b)
print(a * b)
print(a / b)

print(np.sum(a))
print(a[1])

print("--------------------------------------------------------------")

# Access element
print(arr2[0,2])

# Slicing
c = np.array([10,20,30,40,50,60])

print(c[0:3])
print(c[1:])
print(c[:4])

print("-----------------------------------------------------------")

# Slicing in matrix
d = np.array([
    [1,2,3],
    [4,5,6],
    [7,8,9]
])

print(d[0])        # first row
print(d[:,0])      # first column
print(d[0:2 , 1:3]) # part of matrix

print("---------------------------------------------------------------")

# Editing array
e = np.array([500,60,70,80,90])
e[3] = 100
print(e)

print("--------------------------------------------------------------")

# Random values
print(np.random.rand(5))
print(np.random.rand(10,5))
print(np.random.randint(1,10,5))

print("-----------------------------------------------------------------")

# Statistics
w = np.array([8,9,6,7,5])

print(np.max(w))
print(np.min(w))
print(np.mean(w))
print(np.median(w))
print(np.std(w))

print("----------------------------------------------------------------------")

# Filtering
p = np.array([20,30,50,81])

print(p > 25)
print(p[p > 25])

# Broadcasting
print(p + 5)

print("--------------------------------------------------------------------")

# Matrix multiplication
o = np.array([
    [1,2],
    [5,8]
])

u = np.array([
    [5,6],
    [10,6]
])

print(np.dot(o,u))

print("-----------------------------------------------------------------------")

# Transpose
r = np.array([
    [50,55,8,89],
    [60,90,70,66]
])

print(r.T)

# Flatten
print(r.flatten())

print("-------------------------------------------------------------------------")

# Save data
np.save("data.npy", r)

# Load data
loaded = np.load("data.npy")
print(loaded)

print("------------------------------------------------------------------------")

# Unique values
arr_unique = np.array([1,2,2,3,4,4,5])
print(np.unique(arr_unique))

print("------------------------------------------------------------------------")

# Rounding functions

arr22 = np.array([1.2, 2.6, 3.5, 4.1])
print(np.round(arr22))  # np.round: rounds each element to the nearest integer

arr33 = np.array([1.9, 2.3, 3.7, 4.1])
print(np.floor(arr33))  # np.floor: rounds each element down to the nearest integer (floor)

arr44 = np.array([1.2, 2.3, 3.8, 4.1])
print(np.ceil(arr44))   # np.ceil: rounds each element up to the nearest integer (ceiling)

arr55 = np.array([1.9, 2.3, 3.7, 4.1])
print(np.trunc(arr55))  # np.trunc: truncates the decimal part, keeping only the integer part
مم
