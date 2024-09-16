# Experiment 2: Numerical Python (NumPy)
## Course: ECE 2112 - Advanced Computer Programming and Algorithms
#### University of Santo Tomas, Electronics Engineering Department
---
## Introduction
The second experiment for ECE 2112: Advanced Computer Programming and Algorithms contains library name "NumPy". For this experiment, the programmer will deal with Numerical Python or also known as NumPy. It is the core library for scientific computing in Python. It provides a high-performance multidimensional array object and tools for working with arrays. 

## Intended Learning Outcomes
This experiment deals with two learning outcomes, mainly:
To identify the codes and functions incorporated in the Numpy library.
To be able to apply and use the different codes and functions in creating a Python program using a Numpy library.

## Summary of Problems
#### Normalization Problem
- Background: Normalization is one of the most basic preprocessing techniques in data analytics. This involves centering and scaling process. Centering means   subtracting the data from the mean and scaling means dividing with its standard deviation. Mathematically, normalization can be expressed as: </br>
![image](https://github.com/user-attachments/assets/b1ed4767-6e27-4403-b9a2-fe1ab05bb65d)

- Instructions: Create a random 5x5 ndarray and store it to variable X. Normalize X. The normalized ndarray file should be named as X_normalized.npy

- Code sample:
```
#Import numpy library
import numpy as np

# Create a random 5x5 ndarray
X = np.random.rand(5, 5)

# Calculate the mean and standard deviation
mean_X = X.mean()
std_X = X.std()

# Normalize the array
X_normalized = (X - mean_X) / std_X

# Save as X_normalized.npy and print result
np.save('X_normalized.npy', X_normalized)
print (X_normalized)
```
#### Divisible By 3 Problem
- Instructions: Create the following 10x10 ndarray which are the squares of the first 100 positive integers. From this ndarray, determine all the elements that are divisible by 3. Save the file of the result as div_by_3.npy.

![image](https://github.com/user-attachments/assets/ab5173d4-b6e7-4692-b640-a8067bc32ff8)

- Code sample:
```
#Import numpy library
import numpy as np

# Create a 10x10 array of squares of the first 100 positive integers
A = np.arange(1, 101).reshape(10, 10) ** 2

# Find elements divisible by 3
div_by_3 = A[A % 3 == 0]

# Save as div_by_3.npy and print result
np.save('div_by_3.npy', div_by_3)
print (div_by_3)
```
---
## How can this be related to real-life?
Python has many applications in real-life especially now that the world revolves around the use of technology. Some of the top real-life applications of Python are:
- Web Development
- Game Development
- Artificial Intelligence
- Data Science
- Audio and Visual or Image Processing

## Best Practices To Do When Coding
When coding, it is best to do practices that would help you efficiently write codes. The top 5 best practices when coding in Python are:
- Usage of descriptive variable names.
- Usage of variables for constants.
- Leaving comments and taking documentation.
- Usage of whitespace.
- Be consistent with the codes.
---
## Files Included
- Tabora-EXPERIMENT 2.ipynb: Jupyter notebook with the Python code.
- X_normalized.npy: Output file containing the normalized ndarray.
- div_by_3.npy: Output file containing elements divisible by 3.
---
## Software and Library Used
- Python (version 3.x)
- Jupyter Notebook
- NumPy (Numerical Python Library)
---
## Author
- Carl Johnsen M. Tabora
