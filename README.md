# Background of Problem Statement:
Features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei present in the image.
n the 3-dimensional space is that described in: [K. P. Bennett and O. L. Mangasarian: "Robust Linear Programming Discrimination of Two Linearly Inseparable Sets", Optimization Methods and Software 1, 1992, 23-34].

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

# Dataset Description:
1) ID number
 
2) Diagnosis (M = malignant, B = benign)

Ten real-valued features are computed for each cell nucleus:

a) radius (mean of distances from center to points on the perimeter)

b) texture (standard deviation of gray-scale values)

c) perimeter

d) area

e) smoothness (local variation in radius lengths)

f) compactness (perimeter^2 / area - 1.0)

g) concavity (severity of concave portions of the contour)

h) concave points (number of concave portions of the contour)

i) symmetry

j) fractal dimension ("coastline approximation" - 1)

The mean, standard error and "worst" or largest (mean of the three
largest values) of these features were computed for each image,
resulting in 30 features. For instance, field 3 is Mean Radius, field
13 is Radius SE, field 23 is Worst Radius.

All feature values are recoded with four significant digits.

Class distribution: 357 benign, 212 malignant

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

# Table of metrics for all the algorithms used:


 ![](https://github.com/Dany511/Dany5_portfolio/blob/main/images/Capture.PNG)
 
# Discussions and Conclusions:
For this project, the best Recall score we can get is Recall  = 0.96. Recall also gives a measure of how accurately our model is able to identify the relevant data. We refer to  it as Sensitivity or True Positive Rate. What if a patient has Malignant cancer, but there is no treatment given to him/her because our model predicted so? That is a situation    we would like to avoid!.so the best model we come up with is the Decision Tree Model with high recall value.
