# dataviz-challenge


# Pymaceuticals Inc. Clinical Analysis :

In this assignment, I will apply what I've learned about Matplotlib to a real-world situation and dataset.

## Background 

I have just joined **Pymaceuticals, Inc.**, a pioneering pharmaceutical company that specializes in anti-cancer medications. Recently, the company started screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst, I have been given access to the complete data from the most recent animal study. In this study, 249 mice identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The goal of this study was to compare the performance of Pymaceuticals’ drug of interest, **Capomulin**, against other treatment regimens.

The executive team has tasked me with generating all the tables and figures needed for the technical report of the clinical study. They have also asked for a top-level summary of the study results.

## Executive Summary 

The analysis was conducted on a cleaned dataset comprising 248 mice, assessing the efficacy of various drug regimens in treating SCC. Here are the key findings from the study:

### Summary Statistics 
The drugs Capomulin and Ramicane showed the most promise, having the lowest mean tumor volumes of 40.68 and 40.22 mm³ respectively, and were among the drugs with the highest number of measurements, suggesting robust data. Here is a snapshot of the summary statistics for each drug regimen studied:


### Distribution of Data 
- Capomulin and Ramicane had the highest numbers of observed mouse timepoints per drug regimen, with 230 and 228 respectively.
- The distribution of gender was nearly balanced with 958 males and 922 females participating in the study.

### Final Tumor Volume Analysis 
- Capomulin and Ramicane also reported the lowest final mean tumor volumes at approximately 38 mm³ and 37 mm³, respectively, indicating superior performance in tumor reduction.
- Infubinol and Ceftamin had higher final mean tumor volumes at about 60 mm³ and 59 mm³, respectively, with Infubinol displaying one outlier, suggesting variability in its efficacy.

### Correlation and Regression Analysis 
- The study demonstrated a strong correlation between mouse weight and average tumor volume, with a Pearson's correlation coefficient of 0.842, indicating that higher weight is associated with larger tumor volumes.

### Visual Analysis 
- Line plots of tumor volume over time for Capomulin-treated mice showed a decrease in tumor volume over 45 days, illustrating the treatment's effectiveness.
- The regression analysis on the scatter plot of mouse weight versus average observed tumor volume for Capomulin regimen further supports the strong correlation between these variables.

These findings suggest that Capomulin and Ramicane are significantly more effective in reducing tumor size compared to other treatments in the study. Further studies are recommended to explore the long-term effects and potential for broader application of these treatments.

## Data Analysis Tasks 

### Prepare the Data
- Run the provided package dependency and data imports, then merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.
- Display the number of unique mice IDs in the data, then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. I will use this cleaned DataFrame for the remaining steps.
- Display the updated number of unique mice IDs.

### Generate Summary Statistics 
- Create a DataFrame of summary statistics that includes:
  - A row for each drug regimen, with the regimen names in the index column.
  - Columns for the mean, median, variance, standard deviation, and SEM of the tumor volume.

### Create Bar Charts and Pie Charts 
- Generate two identical bar charts showing the total number of measurements for each drug regimen throughout the study.
  - The first bar chart using the Pandas `DataFrame.plot()` method.
  - The second bar chart using Matplotlib's `pyplot` methods.
- Generate two identical pie charts showing the distribution of female versus male mice in the study.
  - The first pie chart using the Pandas `DataFrame.plot()` method.
  - The second pie chart using Matplotlib's `pyplot` methods.

### Calculate Quartiles, Find Outliers, and Create a Box Plot 
- Calculate the final tumor volume of each mouse across four promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin.
- Calculate the quartiles and IQR and determine any potential outliers across all four treatment regimens.
- Generate a box plot that shows the distribution of the final tumor volume for all mice in each treatment group, highlighting any potential outliers by changing their color and style.

### Create a Line Plot and a Scatter Plot 
- Select a single mouse treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.
- Generate a scatter plot of mouse weight vs. average observed tumor volume for the entire Capomulin regimen.

### Calculate Correlation and Regression 
- Calculate the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin regimen.
- Plot the linear regression model on top of the scatter plot.

