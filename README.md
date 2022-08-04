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
We created a databased in RDS and imported the data in the tables using the following code: [Connect_AWSdb_create_tables.ipynb](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/49c17b05d3aee51411c5ec0fdaf988c5ed866088/Connect_AWSdb_create_tables.ipynb)

## 4. Data Preparation (including cleaning & connection)
### Connection
This code was used to connect to the DB: [WriteDFstoPython](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/4919ab143ab1a628c4d748a802de57bbd8bc4b62/Write_DFs_From_Tables.ipynb)

### Cleaning
This code was used to clean the data: [CleaningDFs](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/ad4e5b28c205a66e2c77e338cc167ae48f1b0bb8/DFs_From_Tables.ipynb)

## 5. Exploratory Data Analysis


## 6. Machine Learning
This code was used for our machine learning model: [MachineLearningModel](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/main/Model_Code_Phase_1.ipynb)
 - The data preprocessing consisted of cleaning the dataframes. We replaced the null values with a value of 0 in our electric car sales dataframe. We also filtered the data for each model prediction we are going to be making. 
 - Our feature selection includes oil prices, 3 features of the car (range, recharge rate, efficiency), and number of charging stations. The decision-making process is that these features under a machine learning model will be able to target and predict the output of electric car sales respectively. 
 - The data was split into a training set with X_train and y_train as our input and target data respectively. 
 - The models we are choosing are Linear Regression for a single feature and multiple Linear Regression. We chose this since it was the most simple and baseline model to choose from that would give us a continuous value as our prediction(ie. Electric Car Sales). Some of its limitations is linked to the features used, meaning that the model is only as good as the features we have chosen to use. 
 - Our end goal is to see what out of these features is able to predict electric car sales accurately by comparing each of the models individually. 

## 7. Dashboard
We used Tableau to create our dashboard and the results can be found here:
1. [Team 5 Dashboard](https://public.tableau.com/app/profile/natalie.legere/viz/Team5GroupProject-EVCARS/Story1?publish=yes)
2. [Month Over Month EV Car Sales vs Gas Prices](https://public.tableau.com/app/profile/natalie.legere/viz/2015to2019MoM/2015to2019MoMElectricCarsvsFuelPrices?publish=yes)

## 8. Results/Findings
In conclusion, our findings are:
- Gas prices did not have any effect on electric car sales in the US
- We are able to predict electric car sales over the next year based on XXX
- Our prediction on gas prices over the next year is limited to XXX
- Increase in electric car sales and available infrastructure go hand in hand

In order to better predict gas prices, other factors would need to come into play for our model (e.g., pandemic, supply, demand, global unrest).  
To improve our prediction on electric vehicle sales, additional data on lithium battery availability

