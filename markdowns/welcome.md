# Machine Learning with Java - Part 4 (Decision tree)

In my previous articles, we have seen the  [Linear Regression](https://tech.io/playgrounds/3771/machine-learning-with-java---part-1-linear-regression) , [Logistic Regression](https://tech.io/playgrounds/34a7ecd0a4487577f516d92548af66891284/machine-learning-with-java---part-2-logistic-regression) and [Nearest Neighbor](https://tech.io/playgrounds/5439/machine-learning-with-java---part-3-k-nearest-neighbor). This article focuses on Decision Tree Classification and its sample use case.

# Decision Tree
Decision Trees are a classic supervised learning algorithms. 

A decision tree is a decision support tool that uses a tree-like graph or model of decisions and their possible consequences, including chance-event outcomes, resource costs, and utility. The decision tree algorithm can be used for solving the regression and classification problems too. 

The main goal of decision tree is to achieve perfect classification with minimum number of decision and it is not always possible due to inconsistencies of data.

# Sample Example

Let us consider you are planning to go out for dining , as your friends are visiting but you are hesitant in deciding on which restaurant to choose. Whenever you want to go out for dining you ask Bobby if he thinks you will like that place or not. You give him a list of restaurants that you have visited and tell him whether you liked each restaurant or not (giving a labelled training dataset). Bobby, ask you few questions like, whether you like roof top seating? Does restaurant serve Indian food ?, Is restaurant open till midnight ? Does restaurant have live music and so on to answer your question. It asks you several informative questions to give the reply whether you will like that restaurant or not. In this Bobby is a decision tree for finding your restaurant preferences.

# Types of Decision Trees

1. Classification Trees
2. Regression Trees

# Classification trees

It is the default kind of decision tree used to separate the dataset into different classes.
The response variable is categorical in nature. (2 categories or multiple categories)

Example: We have two variables age and weight .Based on this we are going to determine whether the person will join jym or not.

# Regression Trees

It is used when the response variable is continuous or numerical in nature. This is again classified into linear relationship and nonlinear relationship between the predictors and response.

Example:Predicted price of a consumer good.

# When to use Decision Trees?

The few scenarious where we can use decision tree algorithm are,

1. The decision trees are suited if the training data contains error. Because they are robust to errors.

2. It is used when the training data has missing values. Because they can handle missing values by looking the data into other columns.

# Advantages

The few advantages of decision trees are,

1. Easy to explain.

2. Data type is not constraint as they can handle both categorical and numerical values.

3. Helpful in data exploration as they implicitly perform the feature selection and which is very helpful in predictive analysis.

# Overfitting 

It is the practical problem while building the decision tree model. The module is having an issue of overfitting when the algorithm continues to go deeper and deeper to reduce the training set error with an increased test set error. (Accuracy of prediction goes down)

It mainly happens because of construction of many branches due to irregularities in data. The overfitting can be avoided by using 2 approaches. They are

1. Pre-Pruning
2. Post-Pruning

# Pre-Pruning

It stops the tree constructions bit early.
It is preferred not to split the node ,if its goodness measure is below a threshold value

# Post-Pruning

It goes deeper and deeper in the tree to build a complete tree.

When tree shows the overfitting problem, then the pruning is done as a post-pruning step.We use a cross-validation data to check the effect of our pruning. Using cross-validation data, it tests whether expanding a node will make an improvement or not.Incase if it shows an improvement, then we can continue expanding the node.Otherwise it should not be expanded.

# Decision Tree Demo

@[Id3 and J48 Classifier in Decision Tree]({"stubs": ["src/main/java/com/gg/ml/DecisionTreeDemo.java"], "command": "com.gg.ml.DecisionTreeDemoTest#test"})


# Code Explanation

In the above code, we have used both the Id3 and J48 algorithms. The ID3 could be implemented when we need faster/simpler result without considering all those additional factors in the J48 consider. J48 handles missing values, has more robust splitting and has routines for pruning the tree structure. In short it is an industrial strength decision tree learner.

# Real Time applications using Decision Tree

The few real time applications are,

1. Great use in finance for option pricing
2. Pattern recognition based on decision trees
3. Bank to classify the loan applicants
4. A popular baby product company, used decision tree machine learning algorithm to decide whether they should continue using the plastic PVC in their products.
5. To identify at-risk patients and disease trends.
6. To select the category of question paper based on expert level
7. To take a decision on accepting or rejecting the employment offer


