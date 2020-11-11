# Project1
## M105120312 王磊
## Teammate： M105120315 刘瀚中
## Titanic survival exploration

### Process

 1.Data reading
   
   We use pd.read_csv to read data.
 
 2.Data preprocessing

First print the first few lines of the data to see the situation of the data. After finding that the data is missing, use ‘.replace(to_replace='?',value=np.nan)’and
‘.dropna(how='any') ’to delete rows with missing data.Second, delete columns such as name and fare that are not useful for prediction; at the same time, replace the Sex string  with a numeric value, that is, change male to 1, and female to 0.Then, use the ‘train_test_split module’ in ‘sklearn.model_selection’ to split the data. And 25% of the data is randomly sampled for testing, and the remaining 75% is used to construct the training set.Finally, standardize the segmented data, including the feature data for training and testing.

 3.KNeighbors

I chose to import KNeighborsClassifier from sklearn.neighbors. I use the K nearest neighbor classifier to make category predictions on the test data, and the prediction results are stored in the variable ‘y_predict’. I use the evaluation function that comes with the model to evaluate the accuracy. Finally, output more detailed classification performance.

 4.DecisionTree
 
 I imported the decision tree classifier from sklearn.tree and initialized the decision tree classifier with the default configuration. Then, I use the segmented training data for model learning. Then, use the trained decision tree model to predict the test feature data. After prediction, import classification_report from sklearn.metrics. Finally, output prediction accuracy and more detailed classification performance.

 5. LogisticRegression & SGDClassifier 
 
 （These two methods are used by my teammate.）
 
### Thoughts And Summary

In the process of writing code, I encountered many problems. For example, due to version reasons, some codes are written in different ways, such as ‘pd.read.csv’ to be modified to ‘pd.read_csv’，need to add parentheses after print, etc.The accuracy of the prediction results of different methods is different, and the accuracy of K nearest neighbor classification is slightly lower than the other three methods, only about 0.93.

Of course, the project we have done still has shortcomings. We did not output a more intuitive chart to show the forecast results, nor did we make a detailed comparison of the four methods, which still needs improvement.

