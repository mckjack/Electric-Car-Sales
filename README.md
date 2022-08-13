# Project-Data-Analytics-Group5

## 1. Project Overview
Our presentation is available here: [Project Data Analytics Group 5 Presentation](https://docs.google.com/presentation/d/1aUmmhFLKrxk1ZIevb6XBO8-0x8Yc5DKfiZdjPkO4udA/edit?usp=sharing).

**Selected topic:** Electric car sales in the US in relation to gas prices and infrastructure availability 

**Our data is sourced from Kaggle and US Dept of Energy:** 
1. Electric car sales
2. Gas prices
3. Infrastructure availability

**Questions we hope to answer:**
1. Did rising/falling gas prices have any effect on electric car sales in the US?
2. Did answer to #1 vary significantly depending on car models?
3. Can we predict electric car sales over the next year based on available datasets?
4. Can we predict gas prices over the next year?
5. Are electric car sales higher where infrastructure is more available?

We selected this topic due to rising gas prices and we wanted to study how it impacts consumer purchases for automobiles.  Our hypothesis is that the gas prices do impact consumer choices.

## 2. Project Pipeline
Early in the project, we determined our applications to be used and our data pipeline as summarized in below diagram.
![image](https://user-images.githubusercontent.com/100737452/182811664-1a1a78b5-a14e-4d3c-871a-d31e0bf2676d.png)

## 3. Database/Storage (along with ERD)
### ERD
![image](https://user-images.githubusercontent.com/100737452/179638294-800abcb7-d0b4-4ac2-82b5-e4c165a400d9.png)

### Database
1. We created a PostgreSQL database on Amazon RDS 
![Create_DataBase](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/data_analystics_project_ning/Images/Create_Database.png)

2. We connected to the database and created tables using the following code: [Connect_AWSdb_create_tables.ipynb](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/49c17b05d3aee51411c5ec0fdaf988c5ed866088/Connect_AWSdb_create_tables.ipynb)

3. We imported the data in the tables with PgAdmin
![Import_csv_to tables](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/data_analystics_project_ning/Images/Import_csv_to%20tables.png)

## 4. Data Preparation (including cleaning & connection)
### Write DataFrames From Tables
We connected to the database and read data of tables into Pandas DataFrames using the following code:: [Write_DFs_From_Tables.ipynb](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/4919ab143ab1a628c4d748a802de57bbd8bc4b62/Write_DFs_From_Tables.ipynb)

### Cleaning
This code was used to clean the data: [CleaningDFs](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/ad4e5b28c205a66e2c77e338cc167ae48f1b0bb8/DFs_From_Tables.ipynb)

## 5. Exploratory Data Analysis
To better understand the data and how each dataset related to each other, we performed the connection through Tableau by importing the cleaned datasets from the previous steps and "joining" the data by date.
![image](https://user-images.githubusercontent.com/100737452/182815679-69b8107f-eb54-49af-8ab5-7fff21f52400.png)
![image](https://user-images.githubusercontent.com/100737452/182815719-38bb5451-6634-4714-a8e7-7e85564c853a.png)


## 6. Machine Learning
This code was used for our machine learning model: [MachineLearningModel](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/main/Model_Code_Phase_2.ipynb)
 - The data preprocessing consisted of cleaning the dataframes. We replaced the null values with a value of 0 in our electric car sales dataframe. We also filtered the data for each model prediction we are going to be making. 
 - Our feature selection includes oil prices, 4 features of the car (range, recharge rate, charging power, and price). The decision-making process is that these features under a machine learning model will be able to target and predict the output of electric car sales respectively. 
 - The data was split into a training set with X_train and y_train as our input and target data respectively. 
 - The models we are choosing are Linear Regression for a single feature and Random Tree Regressor for 4 features. We used Linear Regression to predict car sales using independent variable(oil prices). We used Random Tree Regressor to predict car sales using range, recharge rate, charging power, and price of certain makes and models.
 - During our Linear Regression model we used feature engineering on the sales dataset to see if we could improve the r-squared value. After droppping some columns we achieved an r-squared value of 0.34, so a slight increase but not much. 
 
 Results:
 - Linear Regression r-squared = 0.33
 - Random Tree Regressor = 0.44
 
 Summary:

We see that these models and datasets used did not predict car sales well respectively. This is limited to the features we used to predict these sales and those features were ultimately limited to the data that we found. For example our oil prices and electric car sales data was limited to 2015-2019, meaning that there could be other more recent datasets that could give better accuracy. We can also see that the Random Tree Regressor model did a slightly better job than the Linear Regression model. 

## 7. Dashboard
We used Tableau to create our dashboard and the results can be found here:
1. [Team 5 Dashboard](https://public.tableau.com/app/profile/natalie.legere/viz/Team5GroupProject-EVCARS/Story1?publish=yes)
2. [Month Over Month EV Car Sales vs Gas Prices](https://public.tableau.com/app/profile/natalie.legere/viz/2015to2019MoM/2015to2019MoMElectricCarsvsFuelPrices?publish=yes)

## 8. Results/Findings
In conclusion, our findings are:
- Gas prices did not have any effect on electric car sales in the US
- Based upon machine learning models, features of certain electic car models don't effect sales
- Increase in electric car sales and available infrastructure go hand in hand

In order to better predict gas prices, other factors would need to come into play for our model (e.g., pandemic, supply, demand, global unrest).  
To improve our prediction on electric vehicle sales, additional data on lithium battery availability

