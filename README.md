# Data Analysis and Missing Value Handling Techniques

This repository contains a notebook where I discuss various techniques for dealing with missing values, which are essential in the data cleaning step of any data-driven project. Additionally, I conducted data analysis to gain insights into the datasets used in the project.

# Motivation

The motivation behind this notebook is to provide a comprehensive overview of techniques for handling missing values, which are fundamental to the data cleaning process. By discussing these techniques and performing data analysis, I aim to equip practitioners with the necessary tools to preprocess their data effectively.

# Contents

* We Strated with inprting needed libs.
* Then we loaded data and we made some data exploration.
* We noticed that there are many missing values!!!!! we must deal with it.
* There are several approaches to deal with missing data such as :
    * Remove rows with missing values:
    * Remove columns with a high percentage of missing values.
    * Imputation.
 

# Remove rows with missing values:

We will see if the number of missing values is small compared to the size of our data set so we can simply delete only rows with missing values. However, this approach can lead to loss of valuable data.
we saw that each row containt at least one missing value so we lost all the data set 
=> So this approach must be avoided in our case.

 # Remove columns with a high percentage of missing values:

 This approach aims to drop non critical columns with large proportion of missing values thus we will need to use the threshold concept. The thrshold is the number of missing values from which we can decide to remove a column or not. We will use this formula to calculate the threshold: T = (M/100)*N

   * M : The maximum percentage of missing values per comlumn we can tolorate. In this case we will choose 10%.
   * N : The total number of rows in our data set.
   * T : The threshold.

# Imputation:

It involves filling in missing values with some estimated values. Common methods for imputation include:

   * Mean/Median/Mode imputation: It replaces missing values with the mean, median, or mode of the respective column.
   * Interpolation imputation: Estimate missing values based on the values of neighboring data points.
     
!!! BTW still there are many other imputation methods.

# Usage
The notebook serves as a guide for practitioners looking to preprocess their data effectively. Each technique is accompanied by code examples and explanations to aid understanding and implementation.

#Contributions and Feedback
Feedback, suggestions, and contributions are welcome! If you have any ideas for improvement or additional techniques to include, feel free to open an issue or submit a pull request.

# Imputation depends on the type of the data!!!
For nominal or categorical data the interpolation doesn't make sense coz there is no meaningful order or relationship between the categories.
Instead, we should use other imputation methods such as mode imputation to fill in the missing values as we have seen earlier or we can use binary fill.
