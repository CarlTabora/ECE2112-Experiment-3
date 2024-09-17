# Experiment 3: Python Data Analysis (pandas)
## Course: ECE 2112 - Advanced Computer Programming and Algorithms
#### University of Santo Tomas, Electronics Engineering Department
---
## Introduction
The third experiment for ECE 2112: Advanced Computer Programming and Algorithms contains library name "Pandas". For this experiment, the programmer will deal with Python Data Analysis or also known as Pandas. It is the core Python library that provides high-performance, easy-to-use data structures and data analysis tools for the Python programming language

## Intended Learning Outcomes
This experiment deals with two learning outcomes, mainly:
- To identify the codes and functions incorporated in the Pandas library
- To be able to apply and use the different codes and functions in creating a Python program using a Pandas library

## Summary of Problems
### Instructions: 
For this programming assignment, download the following file and save to your default user folder: http://bit.ly/Cars_file

### Problem 1
- Using knowledge obtained from the experiment and demonstrations:
    - Load the corresponding .csv file into a data frame named cars using pandas
    - Display the first five and last five rows of the resulting cars.

- Code sample:
```
#Import panda library
import pandas as pd

#Reading and loading csv file into a data frame
cars = pd.read_csv('cars.csv')
slice = cars.head()

#Displaying first and last 5 rows of the resulting cars
head_tail_slice = list(range(5))+list(range(-5,0))
cars.iloc[head_tail_slice]
```
### Problem 2
- Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and indexing operations.
    - Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7...) of cars.
    - Display the row that contains the ‘Model’ of ‘Mazda RX4’.
    - How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?
    - Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have

- Code sample:
```
#Import panda library
import pandas as pd

#Reading and loading csv file into a data frame
cars = pd.read_csv('cars.csv')

#Displaying first 5 odd-numbered columns of the resulting cars
cars.iloc[:5,::2]

#Displaying the row that contains the ‘Model’ of ‘Mazda RX4’
cars.loc[cars['Model']=='Mazda RX4']

#Displaying the number of cylinders in the car model "Camaro Z28" have.
cars.loc[cars['Model']=='Camaro Z28',['Model', 'cyl']]

#Displaying the number of cylinders and type of gear in the car model "Mazda RX4 Wag."
models = cars.loc[(cars['Model'] == 'Mazda RX4 Wag') | (cars['Model'] == 'Ford Pantera L') | (cars['Model'] == 'Honda Civic')]
models[['Model', 'cyl', 'gear']]
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
- Tabora-Experiment-3.ipynb: Jupyter notebook with the Python code.
- cars.csv: Excel data for given problems.
- Tabora_Pandas-P1.py: Output file containing problem 1.
- Tabora_Pandas-P2.py: Output file containing problem 2.
---
## Software and Library Used
- Python (version 3.x)
- Jupyter Notebook
- paandas (Python Data Analysis Library)
---
## Author
- Carl Johnsen M. Tabora
