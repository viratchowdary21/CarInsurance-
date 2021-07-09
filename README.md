# CarInsurance
## Introduction:
Every Business runs with risk. When securing a new customer, an insurance company must estimate the risk involved. The risk of car insurance depends on various factors such as income, credit score, model of the car and its purchase The company can avoid adding potentially loss-making customers by predicting the chances of an insurance claim. Furthermore, it helps determine correct monthly charges from insured people or objects. Using the details of the car, I built a model to predict the likelihood of loss-making insurance deals for a car insurance company. In this project, the major challenge is the imbalanced data that leads to distorted results due to bias. I try to increase the percentage of claims by using the over-sampling technique. Further, I have implemented different classification models.
 
## Visualizing data:
1.  proportion of customers with a credit score below 0.2 claimed in the last year remains: 1 / 11
2.  the average number of speeding violations among customers with driving experience between 20 and 29 years is 5794.
3.  the no. of customers who drive sports are 477
4.  standard deviation of annual mileage is 2818.434528.
 
        There are many categorical features are existing in data, with those it is possible to distinguish customers such as race, income, education and so on. Claimants are common in the region and annual mileage. According to data, region 10238 is a profitable location for the client. 
 
            No client did not have enough data. Most of the data is biased to one kind of data, it is imbalanced data. It can be resolved by applying oversampling. Oversampling creates duplicates or fake data of the minor data (less data). Those who have more data are those absolutely wins. Collect more data. Do more surveys and feedback from the customers.
 
## Modelling:
      I had implemented feature extraction to select the best 12 out of 17 features. Feature Extraction uses existing features to create new ones from a dataset, then discards the original points. These reduced sets of features will then be able to cover most of the original set of features. I have implemented goodness of fit (chi-square test) and recursive feature elimination method (RFE). And then I shortlisted based on RFE. 
            I have performed 3 different models. They are machines learning models, over-sampling and further TensorFlow binary classification model.
 
Machine learning Classification Models:
Models are called either interpretable or flexible. 
noise	Best case	Worst case	Hypothesis degree
bias	interpretable	Underfitting	low
variance	flexible	Overfitting	high

            Based on the 80/20 rule, I split the data into train and test. I have implemented 7 ML algorithms with little hyperparameter tuning. I applied score test, classification report and roc area under the curve and then I extracted the overall ML algorithms metrics summary.
 
## ML models with over-sampling:
            I used SMOTE from imbalance learn (imblearn) library to perform over-sampling. One can ask why over-sampling rather than under-sampling? We can indeed use any. Over-sampling is based on creating minor data duplication and under-sampling is about the deletion of major data. Doing under-sampling leads to loss of data and we also have fewer data (10k). so, it’s better to perform over-sampling.
 
            For example, Imbalanced data (over-sampling) is a higher education reservation. The percentage lower caste literacy rate is low, so the government is allowed to provide reservations for them. For under-sampling is a kind of tax system (I do not need to explain this, everyone knows). 
 
## Tensorflow Model- binary classification:
            Tensorflow is applicable for many high-level languages and Keara is that one of the most popular python modules. This is a 4-layer model (not including the input layer). There two types of activation functions, one is monotonic, and the other is non-monotonic (RBF). in this notebook, I have used only monotonic activation functions. For hidden layers I used ReLU and for the output layer, it is sigmoid. For callbacks, I sued early stopping. I have applied few metrics and then created a data frame for the metrics and plot different metric plots (not many)
 
How to perform predictions with unseen data?
Code: test_prediction = tf_model.predict(X_test)
  I not going to make any interface for this notebook (flask). In the above, there is code right, in that X_test is there. We need to fill the data according to X_test features and shape and then put them into a list. Replace the X_test with the unseen data list, model. predict passed to the data trained model and gave reasonable predictions.

