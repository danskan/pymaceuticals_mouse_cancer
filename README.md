# pymaceuticals_mouse_cancer

Observations are at the top of the "pymaceuticals_final" file.
Graphs are located in the Results directory

## Instructions

Your tasks are to do the following:

### Initial Preparation

* Run the provided package dependency and data imports, then merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.

* Display the number of unique mice IDs in the data, then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, then create a new DataFrame where this data is removed. 

* Use this cleaned DataFrame for the remaining steps.

* Display the updated number of unique mice IDs.

### Summary Statistics

* Create two summary statistics tables:

    * For the first table, use the `groupby` method to generate the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen. This should result in five unique series objects. Combine these objects into a single summary statistics table.
    * For the second table, use the `agg` method to produce the same summary statistics table using a single line of code.

### Bar and Pie Charts

* Generate two bar plots:

    * Both of these plots should be identical and should show the total number of timepoints for all mice tested for each drug regimen throughout the course of the study.
    * Create the first bar plot using Pandas's `DataFrame.plot()` method.
    * Create the second bar plot using Matplotlib's `pyplot` methods.

* Generate two pie plots:

    * Both of these plots should be identical and should show the distribution of female or male mice in the study.
    * Create the first pie plot using both Pandas's `DataFrame.plot()`.
    * Create the second pie plot using Matplotlib's `pyplot` methods.

### Quartiles, Outliers and Boxplots

* Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Calculate the quartiles and IQR and quantitatively determine if there are any potential outliers across all four treatment regimens.

    * Start by creating a grouped DataFrame that shows the last (greatest) time point for each mouse, then merge this grouped DataFrame with the original cleaned DataFrame.
    * Next, create a list that holds the treatment names, as well as a second, empty list that will hold the tumor volume data.
    * Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list. Determine outliers using the upper and lower bounds, then print the results.
    
* Using Matplotlib, generate a box and whisker plot of the final tumor volume for all four treatment regimens and highlight any potential outliers in the plot by changing their color and style.

  **Hint**: All four box plots should be within the same figure. Use this [Matplotlib documentation page](https://matplotlib.org/gallery/pyplots/boxplot_demo_pyplot.html#sphx-glr-gallery-pyplots-boxplot-demo-pyplot-py) for help with changing the style of the outliers.

### Line and Scatter Plots

* Select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.

* Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

### Correlation and Regression

* Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. Plot the linear regression model on top of the previous scatter plot.
