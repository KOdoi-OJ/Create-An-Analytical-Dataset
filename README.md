# Create-An-Analytical-Dataset
## Project Overview

This is the 3rd project in Udacity's Predictive Analytics Nanodegree.
This project is the first part of a two-part series. In the first part, you will blend and format data and deal with outliers.

For the second part, you will use your cleaned up dataset to create another linear regression model. The difference this time is that you will have to choose which variable(s) are the most important for the model using new techniques learned in the Selecting Predictor Variables section.

## Scenario

Pawdacity is a leading pet store chain in Wyoming with 13 stores throughout the state. This year, Pawdacity would like to expand and open a 14th store. Your manager has asked you to perform an analysis to recommend the city for Pawdacity's newest store, based on predicted yearly sales.

### How Do I Complete this Project?

This project uses skills learned throughout the "Data Preparation" lessons. To complete this project:

- Go through the course.
- Apply the skills learned in the course to solve the business problem given in the project details.
- Use our guidelines and rubric to help build your project.
- When you're ready, submit it to us for review using the submission template found in the supporting materials section.

### Skills Required

In order to complete this project, you must be able to:

- Understand different data types.
- Deal with a variety of data issues.
- Format data appropriately.
- Blend data together using joins and unions.

## The Business Problem

Pawdacity is a leading pet store chain in Wyoming with 13 stores throughout the state. This year, Pawdacity would like to expand and open a 14th store. Your manager has asked you to perform an analysis to recommend the city for Pawdacity's newest store, based on predicted yearly sales.

Your first step in predicting yearly sales is to first format and blend together data from different datasets and deal with outliers.

Your manager has given you the following information to work with:

1. The monthly sales data for all of the Pawdacity stores for the year 2010.
2. NAICS data on the most current sales of all competitor stores where total sales is equal to 12 months of sales.
3. A partially parsed data file that can be used for population numbers.
4. Demographic data (Households with individuals under 18, Land Area, Population Density, and Total Families) for each city and county in the state of Wyoming. For people who are unfamiliar with the US city system, a state contains counties and counties contains one or more cities.

**Map of Wyoming Counties**

![](https://video.udacity-data.com/topher/2019/August/5d47a493_wyoming-county-map/wyoming-county-map.gif)


## Steps to Success

### Step 1: Business and Data Understanding

Your project should include a description of the key business decisions that need to be made.

### Step 2: Building the Training Set

To properly build the model, and select predictor variables, create a dataset with the following columns:
> - City
> - 2010 Census Population
> - Total Pawdacity Sales
> - Households with Under 18
> - Land Area
> - Population Density
> - Total Families

This dataset will be your training set to help you build a regression model in order to predict sales in the Practice Project in the next lesson. Every row should have sales data because we're trying to predict sales.

**Notes**

You should be consolidating the data at the city level and  **not at the store level.**  We only have data at the city wide level so any analysis at the store level will not be sufficient to complete this analysis.

We simply need to focus on cleaning up and blending the data together in this step.

If you've done everything correctly, the sum for each of the above columns should be:

- **Census Population:**  213,862
- **Total Pawdacity Sales:**  3,773,304
- **Households with Under 18:**  34,064
- **Land Area:**  33,071
- **Population Density:**  63
- **Total Families:**  62,653

with  **11 rows of data**

For Alteryx users:

- Use the Autofield Tool to help quickly convert your data fields into the appropriate datafields for analysis.
- Research these [three specific formulas](http://help.alteryx.com/10.6/index.htm#Reference/Functions.htm%23String) to help you get rid of unwanted characters in the Formula tool: ReplaceFirst, Left, FindString

### Step 3: Dealing with Outliers

Once you have created the dataset, look for outliers and figure out how deal with your outliers. Use the IQR method to determine if there are outlier cities for each of the variables and then justify which city that has at least one outlier value should be removed.

**IQR Steps**

To calculate the upper fence and the lower fence, here are the exact steps:

1. Calculate 1st quartile Q1 and 3rd quartile Q3 of the dataset. You can use the Excel function QUARTILE.INC or QUARTILE.EXC

2. Calculate the Interquartile Range: IQR = Q3 - Q1

3. Add 1.5 _IQR to Q3 to get the upper fence: Upper Fence = Q3 + 1.5 _IQR

4. Subtract 1.5 _IQR to Q1 to get the lower fence: Lower Fence = Q1 - 1.5 _IQR

5. Values above the Upper Fence and values below the Lower Fence are outliers

## Supporting Materials

### Review

Use the [project rubric](https://review.udacity.com/#!/rubrics/382/view) to review your project. If you are happy with your submission, then you're ready to submit your project. If you see room for improvement, keep working to improve your project.


### Data

- _p2-2010-pawdacity-monthly-sales.csv_ - This file contains all of the monthly sales for all Pawdacity stores for 2010.

- _p2-partially-parsed-wy-web-scrape.csv_ - This is a partially parsed data file that can be used for population numbers.

- _p2-wy-453910-naics-data.csv_ - NAICS data on the sales of all competitor stores where total sales is equal to 12 months of sales

- _p2-wy-demographic-data.csv_ - This file contains demographic data for each city and county in Wyoming.

### Links

- [Competitor Sales](https://github.com/KOdoi-OJ/Create-An-Analytical-Dataset/blob/main/datasets/p2-wy-453910-naics-data.csv)
- [Demographic Data](https://github.com/KOdoi-OJ/Create-An-Analytical-Dataset/blob/main/datasets/p2-wy-demographic-data.csv)
- [Population Data](https://github.com/KOdoi-OJ/Create-An-Analytical-Dataset/blob/main/datasets/p2-partially-parsed-wy-web-scrape.csv)
- [Pawdacity Monthly Sales](https://github.com/KOdoi-OJ/Create-An-Analytical-Dataset/blob/main/datasets/p2-2010-pawdacity-monthly-sales-p2-2010-pawdacity-monthly-sales.csv)

## Results

The final submission for this project can be found [here](https://github.com/KOdoi-OJ/Create-An-Analytical-Dataset/blob/main/Final%20Submission%20-%20Create%20an%20Analytical%20Dataset.pdf)

---
*This project was completed, after final review and approval, on March 20, 2022*

