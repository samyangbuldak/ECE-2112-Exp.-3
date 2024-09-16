# ECE-2112 - Programming Assignment 3
# Experiment 3 - Python Data Analysis (PANDA)
### Getting Started
In this repository, you will find my codes for Experiment 3 containing two problems:
   1. Problem 1 (loading a dataframe)
   2. Problem 2 (performing operations on a dataframe)

The following tools were used in the completion of this experiment:
 - Anaconda Navigator 2.6.0
 - Jupyter Notebook 7.0.8

### Problem 1
This script utilizes the pandas library to load a car dataset from a _`.csv`_ file into a DataFrame using the **_`read_csv()`_** function. It then displays the first and last five rows of the dataset using the **_`head()`_** and **_`tail()`_** functions, respectively, to inspect the data.

### Problem 2
Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and indexing operations.

a. To display the first five rows with odd-numbered columns (columns 1, 3, 5, 7…) from the DataFrame **_`cars`_**, I used the **_`iloc`_** method. Specifically, **_`cars.iloc[1::2].head()`_** was used to select every second row starting from index 1 and then displayed the first five rows of this subset. This approach effectively retrieves and displays the rows from odd-numbered columns, assuming the indexing starts from 1 (1-based index).

b. To display the row that contains the _‘Model’_ of _‘Mazda RX4’_, I used boolean indexing with the _loc_ method. Specifically, **_cars.loc[cars['Model'] == 'Mazda RX4']_** was employed to filter the DataFrame, selecting the row where the** _'Model'_** column matches **_'Mazda RX4'_**. This method efficiently retrieves the specific row corresponding to the given car model.

c. To determine how many cylinders the car model **_‘Camaro Z28’_** has, I used the _loc_ method with boolean indexing. The code **_cars.loc[(cars['Model'] == 'Camaro Z28'), ['Model', 'cyl']]_** filters the DataFrame to select the row where the** _'Model'_** is **_'Camaro Z28'_** and retrieves the values from both the **_'Model'_** and **_'cyl'_** columns. This approach allows for extracting the specific information about the number of cylinders for the given car model.

d. To determine how many cylinders and what gear type the car models **_‘Mazda RX4 Wag’, ‘Ford Pantera L’,_** and **_‘Honda Civic’_** have, I utilized the `loc` method combined with the **_`.isin()`_** function. The code **_`cars.loc[cars['Model'].isin(['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']), ['Model', 'cyl', 'gear']]`_** filters the DataFrame to select rows where the 'Model' is one of the specified car models. It then retrieves the corresponding values for the 'Model', 'cyl', and 'gear' columns, effectively providing the required information for each specified car model.


# Authors
Samantha Louise J. Samoy 

2ECE-C
