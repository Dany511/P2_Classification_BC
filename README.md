# Problem Statement:
Usually classifying the cancer into benign or malignant to proceed further diagnosis  requires a highly experienced doctor. But with the help of the digital image of the cancer cell lump and drawing features from that image gives data to analyse and predict the class of the cancer. After drawing features from several images of wisconsin cancer patients 10 main characteristics were selected and their data was stored. We have the data of 570 unknown breast cancer patients. Using machine learning techniques with python, we are going  to analyse the data and predict the cancer class for the future patients.

# Requirements:
We need jupyter notebook environment for executing python program.

# Packages and libraries required:
pandas,
numpy,
matplotlib,
scikit learn,
seaborn.

# Reading the data:
we will import the raw data which is in csv format from local database using pandas library.

# Handling the missing values: 
As the data was collected from different sources, there may be some missing data which has to be replaced or dropped to get better prediction. here we replace the missing data with the mean of that column. we have to do this operation to all the columns of the dataframe.

# Encoding of categorical values: 
To know the data type of columns , we use dtypes function.from that we get the columns with object data type and we convert them into numerical values.

# Standardisation of data: 
We have to standardize the data to give same level of priority to all features of data. Here we are standardizing the data using sklearn package and StandardScaler library.

# Splitting of data:
We have split  80% of the total data into training dataset and 20% of the total data into test dataset.

# Model Training,Model Testing and Model Evaluation: 
We are going to fit the training data into different classifiers using fit() function.we test every model on the testing data using predict function. we then check the accuracy of the prediction using metrics library of sklearn package.The max accuracy is achieved by svm model ie 0.93671.


 ![](https://github.com/Dany511/Dany5_portfolio/blob/main/images/Capture.PNG)
