---
layout: page
title: "Data Visualizations"
# permalink: /datavisualizations/
---

The Paris-Lille-3D Dataset was selected based on numerous factors. The dataset consists of 50 different classes of more than 140 million objects that were entirely labeled by hand. The large number of classes allows the classification of urban objects of various sizes and shapes.

![Dataset Description](/images/DatasetDescription.png){:class="img-responsive"}

The project findings show that new techniques are not always better. An analysis of different techniques finds that XGBoost, a machine learning method, had the highest accuracy score of 0.9393. The next two highest scores were also with machine learning methods: AdaBoost with .931 and Gradient Boosting with .925. The scores for the deep learning methods, VoxNet and PointNet were 0.7300 and 0.4523 respectively, significantly lower than the scores for the machine learning methods. One can take away from this analysis that deep learning does not always produce better results. It also points to the fact that boosting and ensemble methods perform the best, particularly ones which use decision trees. The Random Forest Ensemble classifier itself scored at .911.

The greatest improvement through hyperparameter tuning is with AdaBoost, going from a baseline score of 0.1311 to an optimized score of 0.9311. In contrast, Gradient Boosting had a very small improvement in the score from 0.9197 to 0.9246.

![Method Accuracy Scores](/images/MethodAccuracyScores.png){:class="img-responsive"}

Data processing was a critical step in the entire project. For the machine learning approach, features had to be calculated by calculating the covariance matrix of an object’s point coordinates and then the matrix’s eigenvalues. These eigenvalues were then themselves used to calculate:

![Geometric Features](/images/GeometricFeatures.png){:class="img-responsive"}

