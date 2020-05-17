# dsiprojects
### Overview

This project seeks to identify the best classification model that can distinguish which of two subreddits a post belongs to. The  performance of 2 parametric models will be evaluated. In the instance of Logistic Regression, the coefficients can be interpreted to identify features that increases the log-odds of a post to be from the positive class, or else being equal.

Advertisors seeking to use reddit as a marketing platform will be able to develop marketing strategies specifically targeted  at each subreddit based on what each community is most concerned about.

Two closely-related subreddits, namely /gainit and /keto are selected to identify the classification model that can more accurately classify the posts to their respective subreddit.

The /gainit subreddit is a fitness subreddit for information and discussion for people looking to put on weight, muscle, and strength.

The /keto subreddit is a place to share thoughts, ideas, benefits, and experiences around eating within a Ketogenic lifestyle.

While seemingly dissimilar, the 2 threads share commonalities.
1. Focus on caloric intake and fitness
2. Macronutrients: The basis of a ketogenic diet is one that focuses on a relatively high-protein, high-fat diet. The increased intake amount of these nutrients are common to what a person seeking to gain muscle/weight would incorporate to attain the one's goal

Moderators of the post can use the model to potentially flag out misclassified posts to maintain the integrity of the posts in the subreddit thread.  

### Datasets

#### Provided Data

The provided datasets are as follows:

- [keto dataset](./datasets/keto.csv)
- [gainit dataset](./datasets/gainit.csv)
- [combined dataset](./datasets/combined.csv)


These are the data obtained from the keto and gainit subreddit. The complete dataset with both datasets is also available.

### Data Dictionary

|Feature|Type|Dataset|Description|
|:---|:---:|:---:|:---|
|selftext|object|combined|The content of the post|
|target|int|combined|the class that the post belongs to|

### Summary

|        Model        |    value of fit_prior   | Penalty |   Hyperparameter   | Training Accuracy | Testing Accuracy |Vectorizer |
|:-------------------:|:--------------:|:-------:|:----------:|:-----------------:|:----------------:|:----------------:|
|         MultinomialNB         |  False |    NA   |      *α* = 1     |       0.967      |      0.896     |CountVectorizer|
|         MultinomialNB         |  False |    NA   |      *α* = 1     |       0.963      |      0.892      |TfidfVectorizer|
| logistic regression |   NA   |  Ridge  |   *C* = 1 |       0.988      |      0.904      |TfidfVectorizer|
| logistic regression |   NA   |  Ridge  | *C* = 0.01 |       0.947      |      0.892      |CountVectorizer|

Taking into consideration the various metrics which includes: accuracy, precision, sensitivity, f1-score and AUC-ROC the logistic regression model fitted with features extracted from unstructured text by fitting and transforming with `TfidfVectorizer` performed the best.
