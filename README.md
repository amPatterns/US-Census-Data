# US Census Data
The dataset contains about 300 000 rows and contains data about individuals , education work, family , race etc from the US Census bureau. The goal is to predict whether an individual earns more than 50K dollars a year or not, and to give clear insights about the profiles of high income earners and visualise the data. The dataset has about 6% individuals who earn more than 50K, thus making the dataset very unbalanced. This project shows how to classify data with numerical and categorical data, on an unbalanced dataset ( 6 % of positives). An important aspect is to have a good recall, as identifying most of the individuals with more than 50k earnings is important, but also a good precision, because we do not want to have too many false positives. Thus, the ROC curves and setting threshold values for the classifier is an important aspect of the problem, and we will choose the f1 score as our performance metric.

The choice of the classifier will be logistic regression, a simple supervised algorithm, and Random Forest, a tree based algorithm. Both models estimate probabilities which will be helpful to set thresholds.

We do a 3 fold cross validation to see the performance of our models.However we are choosing the f1 score as the metric because we have an unabalanced dataset with few positive observations.

The plots of correlation and scatterplots are used to choose which variables we will be keeping, and variables whith a high amount of NUlls are discarded or replaced . Categorical variables are transformed into dummy variables in order to be used by the model.

We choose the parameters for our model using GridSearchCV, from scikit learn.
