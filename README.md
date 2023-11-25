## Raisin Class Prediction: A guideline of Implementing Logistic Regression

Welcome to this comprehensive guideline on implementing Logistic Regression for classification tasks using a real-world dataset. In this tutorial, we will delve into the intricacies of Logistic Regression, a widely used algorithm in the realm of machine learning, particularly for binary classification problems.

## **Dataset Overview**  
The dataset at our disposal comprises images of Kecimen and Besni raisin varieties grown in Turkey. Through the Computer Vision System (CVS), a total of 900 raisin grains were captured, encompassing 450 pieces from each variety. These images underwent various pre-processing stages, resulting in the extraction of seven morphological features. The goal is to classify these features using Logistic Regression and subsequently optimize the model through hyperparameter tuning.

## **Attributes**  
*Area:* The number of pixels within the boundaries of the raisin.  
*Perimeter:* Measurement of the environment by calculating the distance between the boundaries of the raisin and the pixels around it.  
*MajorAxisLength:* Length of the main axis, the longest line that can be drawn on the raisin.  
*MinorAxisLength:* Length of the small axis, the shortest line that can be drawn on the raisin.  
*Eccentricity:* A measure of the eccentricity of the ellipse, which has the same moments as raisins.  
*ConvexArea:* The number of pixels of the smallest convex shell of the region formed by the raisin.  
*Extent:* Ratio of the region formed by the raisin to the total pixels in the bounding box.  
*Class:* Kecimen and Besni raisin (Target Variable).  


## **Outline**  
*Exploratory Data Analysis (EDA):* Conduct an exploration of the dataset, examining key statistics and visualizing the distribution of features to gain insights into the data.  
*Logistic Regression Model:* Build a baseline Logistic Regression model using scikit-learn's pipeline. Train and evaluate the model using standard metrics such as accuracy, recall, F1 score, classification results, and ROC-AUC.    
*Cross-Validation:* Assess the model's performance using cross-validation to ensure robustness and reliability of results.  
*Hyperparameter Tuning:* Employ GridSearchCV to fine-tune the hyperparameters of the Logistic Regression model, optimizing its predictive capabilities.  
*Performance Comparison:* Analyze and compare the results before and after hyperparameter tuning to gauge the effectiveness of the optimization process.  
*Threshold Optimization:* Investigate the best threshold for predicting probabilities, fine-tuning the model for practical deployment. 

## **Key Findings from the Study**
- Classes of raisins in the dataset (target feature) is distributed in balance %50 each observations.
- Apart from the 'extent' feature almost in all features, Besni Raisins have fairly higher values than Kecimen Raisin type.
- For 'extent' variable, while Besni Raisins range is bigger than Kecimen, both Raisin types median extends are similar
- There is an obvious evidence of multicollinearity in our dataset. One important assumptions of logistic regression is that the dataset shouldn't have multicollinearity. However, regularization parametre in LogisticRegression can mitigate this issue. we experimented both scenarios.
- The highest correlations with the classes are Perimeter, Area and AxisLengths. For these features, there are some overlapping values for both classes of raisins
where the correct classification probability of the model were expected to decrease.
- Since our target class is well balanced, its possible to use accuracy score as the metric. Our baseline model with default paramtres have 0.86 accuracy score which means the models predictions are 86% True. Also, we cross validated this findings within different folds.
- After hyperparametre tuning, our model produced an accuracy score of 0.87 on test data, a bit improvement on the scores was seen. Moreover, both models produced a 0.93 ROC-AUC score which we can easily interpret as the ratio of True Positives to False Positives
- The models best treshold is found to be 0.483


## **Contact**  
Reachme for more or discussion from [Linkedin](https://www.linkedin.com/in/fatih-calik-469961237/), [Github](https://github.com/fatih-ml) or [Kaggle](https://www.kaggle.com/fatihkgg) 


**REMINDER:** This notebook aims to serve as a practical and informative guide for data science learners, providing a step-by-step approach to implementing and optimizing Logistic Regression models on real-world datasets. Let's embark on this journey to unravel the nuances of Logistic Regression and enhance our understanding of its application in classification tasks.
