# Data Cleaning 

Proper data cleaning in crucial, it can make or break your project. Data scientist spend a majority of their time in this step. Have you heard the saying "Better data beats fancier algorithm" ? This is true. In other words, garbage in gets you garbage out. 

Please remember: **BETTER DATA > FANCY ALGORITHMS**

Different types of data require different types of cleaning. However, the systematic approach are similar. The general approach is: 
- Remove unwanted observations
- Fix structural errors
- Remove/filter unwanted outliers
- Handle missing data

## Unwanted data
The first step of data cleaning is removing unwanted data from your dataset, which includes duplicate and/or irrelevant observations. 

**Duplicate data**

This happens most often during the data collection step. For example, when you: 1) merge multiple datasets 2) scrape data 3) receive data from other sources i.e. clients or other departments. 

**Irrelevant data** 

Irrelevant observations are the ones that don't fit the specific problem we're trying to solve. For example, when your building a model for public schools systems, you wouldn't want information about private school systems. This is also the time to explore your data and filter out information prior to feature engineering. 

## Fixing structual errors
Here we check for "typos" and mislabeled classes. This happens mostly in categorical features. Structual errors typically arise during measurement, data transfer, or other types of poor data management. 

## Unwanted Outliers
Certain types of models will run into problems if you don't deal with outliers. Linear regression models are less robust than decision tree models. Generally, removing outliers (if there is legitimate reason) will increase your models performance. But, you should never remove an outlier for the sake of removing. Good reason must be accompanied with removal of outliers.

## Missing Data
Simply ignoring mising data is a BIG NO NO. The 2 most commonly recommended ways of handling missing data is either **1) dropping the observations or 2) imputing missing values based on other observations.** 

When dropping missing values, you drop information. 
- Sometimes, missing value may be information in itself
- In the real world, often times predictions on new data are needed even if some features are missing

Imputing missing values can lead to a loss of information. 
- Imputing missing data is does not add "real" information, it's reinforcing the patterns already provided by other values 

### Missing categorical data: 
The best way to handle missing categorical data is to label them as missing. 
- essentially adding a new class for the feature
- informs the algorithm the value was missing 
- technically, no missing values because they're labeled 

### Missing numeric data:
The best way to handle missing numeric data is to flag and fill the values. 
- Flag, indicating its missingness 
- Fill the missing value with a 0 to meet technical requirements of no missing values 
By using this technique, the algorithm can estimate the constant for missingness vs. filling with the mean. 

Proper data cleaning can save a ton of headaches down the road.

