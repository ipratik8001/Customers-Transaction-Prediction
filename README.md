# Customers-Transaction-Prediction
Problem Statement/Tasks Task 1:-Prepare a complete data analysis report on the given data.  Task 2:-Create a predictive model which will help the bank to identify which customer will make transactions in the future.


Dataset Details We were provided an anonymized dataset containing 200 numeric feature variables, the binary target column, and a string ID_code column.

Problem Analysis This is a binary classification problem, and the task is to predict the value of target column in the test dataset.

Metrics This is a classification problem and we can use the confusion matrix to properly evaluate the model results. The confusion matrix is one of the performance measurments used in machine learning classification problems where output can be two or more classes.

It is useful for measuring Recall, Precision, Specificity, Accuracy, and most importantly AUC-ROC Curve.

Exploratory Data Analysis (EDA) At the EDA stage we check for variable data types, missing values, shape of data, and the balance of the target column. Please refer to the EDA section of the notebook for the output/results.

Feature Selection We have 200 features that are mostly uncorrelated.

Removing redundant columns: One unique value columns,ids columns, serial no.

Check for highly correlated features. If the correlation between two numerical features is more than 0.9, we should remove one of them otherwise this will reduce the accuracy of our model.

Visualizations Almost all features follow normalised distribution.

Distribution of all numerical features per each class: The majority of customers did not perform/complete the transaction (179902). There are close to 200 features/variables and we needed to reduce the dimensionality of our dataset.

Dealing Imbalanced Data Before modelling for this dataset we needed to deal with the imbalanced data. The conventional model evaluation methods do not accurately measure model performance when faced with imbalanced datasets. Standard classifier algorithms like Logistic Regression, Random Forest, and k-NN have a bias towards classes which have large number of instances.

Therefore, there is a high probability of misclassification. The SMOTE technique was used to balance the data.

Model Creation Step 1: Create X (independent variable), and y (dependent variable) Step 2: Apply any feature transformation method based on algorithm Step 3: Create training and testing data Step 4: Compare actual testing and predicted testing values and analyze the performance of model.

Logistic Regression

Logistic Regression is used when the dependent variable (target) is categorical. It has a bias towards classes which have large number of instances and tends to only predict the majority class data. The features of the minority class are treated as noise and are often ignored. Therefore, there is a high probability of misclassying the minority class.

We are unable to properly comment on the business aspect because of the dataset was encrypted for security reasons. This is a legitimate limitation. The Logistic Regression accuracy was 90%.

K-NN

The k-nearest neighbors algorithm is a non-parametric,supervised learning classifier. It uses proximity to make classifications or predictions about the grouping of an individual data point.

The K-NN model accuracy was 89% and we noted that it took a long time to execute.

Random Forest

Random Forest is a bagging based ensemble learning model. Random forest is slow because it has multiple decision trees. Whenever it makes a prediction, all the trees in the forest have to make a prediction for the same given input and then perform voting on it. This consumes lots of time and resources. The result (AUC-score) is not modified if num round would increase the score will be better but speed will be very slow.

The Random Forst accuracy was 89% and we noted that it took long to execute.

XGBoost

XGBoost is Gradient Boosting ensemble model which is faster in speed and accuracy as compared to bagging and adaptive boosting.

Model Comparison Report Below are the algorithms used and their accuracy levels: Logistic Regression : 90% Logistic Regression (PCA) : 91% K-NN (before balancing) : 89% K-NN (after balancing) : 17% Random Forest : 90%

Challenges Faced

Data is completely encrypted with some numerical values,it is not giving much more insight about the customers or information being collected.

Execution time of Random Rorest and K-NN took a long time. We recommend adequate hadware resources if these algorithms will be used on this dataset for similar problems.
