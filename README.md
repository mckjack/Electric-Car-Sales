# Project-Data-Analytics-Group5

### SEGMENT 2

Our **draft** presentation is available here: [Project Data Analytics Group 5 Presentation](https://docs.google.com/presentation/d/1aUmmhFLKrxk1ZIevb6XBO8-0x8Yc5DKfiZdjPkO4udA/edit?usp=sharing).

## 1. Create database in RDS/MongoDB (or a database of your choice) along with tables from the ERD and the data imported in the tables.
This code was used to create our DB: [Connect_AWSdb_create_tables.ipynb](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/49c17b05d3aee51411c5ec0fdaf988c5ed866088/Connect_AWSdb_create_tables.ipynb)

## 2. Python code connecting to the database and getting bringing data back in Python.
This code was used to connect to the DB: [WriteDFstoPython](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/4919ab143ab1a628c4d748a802de57bbd8bc4b62/Write_DFs_From_Tables.ipynb)

## 3. Python/R/Tableau to perform Exploratory Data Analysis (understanding the data and the relationship within the data)
This code was used to clean the data: [CleaningDFs](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/ad4e5b28c205a66e2c77e338cc167ae48f1b0bb8/DFs_From_Tables.ipynb)

**Tableau Presentation plan**
![image](https://user-images.githubusercontent.com/100737452/181134805-2ce4fdfa-111c-4ebe-b656-6acfc15826ad.png)


## 4. Python code for training and testing the benchmark (simple) machine learning model as per your Segment 1 deliverable e.g. Logistic Regression for classification, Kmean for clustering etc.
This code was used for our machine learning model: [MachineLearningModel](https://github.com/mckjack/Project-Data-Analytics-Group5/blob/main/Model_Code_Phase_1.ipynb)
 - The data preprocessing consisted of cleaning the dataframes. We replaced the null values with a value of 0 in our electric car sales dataframe. We also filtered the data for each model prediction we are going to be making. 
 - Our feature selection includes oil prices, 3 features of the car (range, recharge rate, efficiency), and number of charging stations. The decision-making process is that these features under a machine learning model will be able to target and predict the output of electric car sales respectively. 
 - The data was split into a training set with X_train and y_train as our input and target data respectively. 
 - The models we are choosing are Linear Regression for a single feature and multiple Linear Regression. We chose this since it was the most simple and baseline model to choose from that would give us a continuous value as our prediction(ie. Electric Car Sales). Some of its limitations is linked to the features used, meaning that the model is only as good as the features we have chosen to use. 
 - Our end goal is to see what out of these features is able to predict electric car sales accurately by comparing each of them individually. 

### SEGMENT 1

## 1. Database Mock Up (Preferably a ERD - Entity Relationship Diagram)
![image](https://user-images.githubusercontent.com/100737452/179638294-800abcb7-d0b4-4ac2-82b5-e4c165a400d9.png)


## 2. Github repo and everyone has merged with the main branch at least once
Everyone in our project team has merged to the main branch: ![image](https://user-images.githubusercontent.com/100737452/179632030-62c03404-f0aa-421b-b06b-240559ba574a.png)

## 3. Proposed findings and a hypothesis of results (i.e. business problem contextualized with data driven results)
Using the following datasets...
1. Crude oil prices
2. Electric car sales

Questions we hope to answer in our project are:
1. Did rising/falling gas prices have any effect on electric car sales in the US? 
2. Did answer to #1 vary significantly from different states?
3. Can we predict electric car sales over the next year based on the 2 datasets?
4. Can we predict crude oil prices over the next year?

We selected this topic due to rising gas prices and we wanted to study how it impacts consumer purchases for automobiles.  Our hypothesis is that the gas prices do impact consumer choices.

## 4. Diagram of Data Pipeline (ETL, Database, and Machine Learning model)
![image](https://user-images.githubusercontent.com/100737452/179631920-3db32829-3576-46e6-b218-e2d0657f6d25.png)
- We decided based upon our hypothesis and dataset variables that a time-series regression model would be the most ideal model going forward. From the generated database we will use this model to predict the total number of electric cars sold in a given time frame. 
