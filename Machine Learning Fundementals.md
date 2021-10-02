
# Contents:
- Cross validation
- Confusion Matrix
- Sensitivity vs specificity 
- Bias and Variance


## Cross validation

Lets say we have variables **height, age , weight** to predict **health**
We can use logistic regression or k nearest neighbor or support vector machines or any ML Method

**Cross validation** allows us to compare different machine learning methods and get a sense of how well they will work in practice

With the data we have we need to do 2 things:

1) Estimate the parameters for the machine learning methods or "train the algorithm"

**NEVER USE ALL THE DATA TO TRAIN THE ALGORITHM** bc you wont have any data to test the algorithm


2) Evaluate how well teh machine learning methods work. or "testing the algorithm"

Imagine we split the data into 4 blocks 75% of the data for training and the last 25% for testing

### But how do we know that the first 75% of the data we used is the best way to divide the data?

**Crossvalidation** uses all possiblities of dividing the data one at a time and then summarizes the results at the end


At the end we can see how every block of data is used for testing and can **compare** ML methods to see how well they preformed
![image.png](attachment:image.png)

Terminology:
In the example above we divided the data into 4 blocks this is called **Four fold Cross validation**
  the number of blocks is arbitrary
  
**ten fold cross validation** is dividing the data into 10 blocks  
In extreme cases we could seperate each individual into a block this is called **leave one out cross validation**  


## Confusion Matrix
Another way to determine different machine learning methods is by using a confusion matrix

it checks performance measurement for machine learning classification
![image.png](attachment:image.png)


The rows in a confusino matrix corresponds to what the machine learning algorithm predicted

The colums coresponds to the known truth


![image.png](attachment:image.png)




We can see that the random forest was better than the k nearest neighbors in predicting the patients (142 vs 107)

and worse at predicting patients without Heart disease 110 vs 79

**So from the picture above we would choose the random forest over the K-nearest Neighbors**

###  Ultimately, the size of the confusion matrix is determind by the number of things we want to predict.

## Sensitivity vs Specificity

![image.png](attachment:image.png)
Sensitivity tells us what percentage of patients were correctly identified

![image.png](attachment:image.png)
tells us what percentage without heart disease that were correctly identified

**Depending on if you want to identify patients with or without heart disease the model you will differ**

### Ultimatley we can use sensitivity and specificity to help us decide which machine learning method would be best for our data

TLDR:

If correctly identifying **positives** is the most important thing to do with the data you should use the method with the higher **Sensitivity**

If correctly identifying **negatives** is the most important thing to do with the data you should use the method with the higher **Specificity**


## Bias and varaince
imagine a data set of height vs weight
![image.png](attachment:image.png)
Lets say we use Linear regression(red line) to try to predict the data

![image.png](attachment:image.png)
**The straight line doesnt have the flexibility to accuratly replicat the arc in the true relationship no matter how well you fit it to the training set**

The inability for a machine learning method (in this case linear regression) to capture the true relationship is called **Bias**

We can calculate Sum of squares to account for different predictive lines you need to calculate SS on **BOTH** the training data set and the testing data set

### Variance
In machine learning the differences in fits between datasets(training vs testing) is called variance 

***Terminology*** 
If the line fits the **training set** really well but not the **testing set** we say that the line is **overfit**


**Ideally we want a model that has low Bias and Variability we need to find the sweet spot between a simple model and a complex model**

***Terminology*** 

Three commonly used emthods for finding the sweet spot between simple and complicated modesl are called"
**Regularization, Boosting, and bagging**

*Random forest will show an example of bagging in action refer to that skill*



```python

```


```python

```


```python

```
