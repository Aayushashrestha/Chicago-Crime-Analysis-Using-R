# Chicago-Crime-Analysis-Using-R

## Problem Statement
Crime is a significant social problem, and Chicago like many other cities has faced challenges in addressing high crime rate. Law enforcement agencies are constantly seeking ways ot improve their crime prevention and solving. One promising approach is the uttilization of data mining techniques, particularly in crime analysis, which has emerged as a valuable asset in this field. In this project we delve into the application of machine learning in cirme analysis and how it an assist law enforcement agencies in Chicago in predicting and comprehending arrest decisions within the context of crime prevention and solving. 

## Dataset Description
The dataset is obtained from the publcily available Chicago Data Portal, which contains data spanning from 2001-Present. The dataset contains 22 variables that provide detailed information about the various types of crime committed in Chicago. Some of the variables present in the dataset include Date, Crime Type, Description, Location, Arrest, Beat, Domestic etc. These variables capture relevant information such as the date of the crime occurrence, the type and description of the crime, the location where the crime was reported, whether an arrest was made, the community area in which the crime occurred, the police beat number etc. 
The response variable "Arrest" is a binary response variabel that indicates whether an arrest was made in conncetion to the reported crime. This variable serves as a target variable for the ML models which will be trained to predict whether an arrest is likely to occur based on the values of other variables in the dataset. The dataset provides a rich source of information for building predictive models to forecast arrests and allows for extensive analysis of different variables to identify patterns, trends and relations that contribute to the development of accurate and reliable ML models to predict arrest. 

## Approach
### Data Cleaning and Preprocessing
1. Dropped null/missing values.
2. Filtered out irrelevant features
3. Variable Date has been segregated into Day, Month and Weekday variables
4. Combined similar crime type into one to reduce the number.

### Exploratory Analysis
Before fitting the predictive models, an exploratory data analysis (EDA) was conducted to gain a better understanding of the Chicago Crime dataset. The EDA process involved various data visualization and statistical techniques to explore the data, identify patterns, and uncover insights. 
![image](https://user-images.githubusercontent.com/21006311/233501445-6bd8383d-0925-43ea-b1cd-34c5543c004d.png)
![image](https://user-images.githubusercontent.com/21006311/233501463-74cb04d0-2477-4f49-9201-52e69d42bdb6.png)
![image](https://user-images.githubusercontent.com/21006311/233501478-5d7d0a93-4769-42f1-b7ac-f578fbbdafca.png)
![image](https://user-images.githubusercontent.com/21006311/233501489-7eff0b20-2c5b-4764-aa7c-2914c8f2a8bf.png)


### Model Fitting
The preprocessed dataset from the Chicago Crime dataset was divided into training and testing data in an 80:20 ratio. This means that 80% of the data was used for training the K-nearest neighbors (KNN) model, and the remaining 20% was kept aside for testing the model's performance.

The purpose of splitting the dataset into training and testing data is to evaluate the performance of the model on unseen data. The training data is used to train the model, and the testing data is used to assess the model's ability to generalize and make accurate predictions on new, unseen data.
The preprocessed data from the Chicago Crime dataset was then used to train a K-nearest neighbors (KNN) model with K=5. KNN is a popular and simple supervised machine learning algorithm used for both classification and regression tasks.

In the context of this project, since the goal is to predict the type of crime (a multi-class classification task) based on the available features, the preprocessed data, which may have undergone data cleaning, feature engineering, and other necessary transformations, was used as input to the KNN model.

The KNN algorithm works by finding the K nearest neighbors to a new data point in the feature space and then making a prediction based on the majority class or average of the neighbors. The value of K represents the number of neighbors to consider when making predictions. In this case, K=5 was chosen as the hyperparameter for the KNN model, meaning that the model will consider the 5 closest neighbors when making predictions.






