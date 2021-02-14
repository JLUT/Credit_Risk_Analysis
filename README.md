# Credit_Risk_Analysis



**Overview of the Analysis**


In this challenge, we built and evaluated six machine learning models to assess credit risk.
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we have used different techniques to train and evaluate models with unbalanced classes and used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.



**Results**



The balanced accuracy scores and the precision and recall scores of all six machine learning models.

For any machine learning model, we first start with converting our string values into numerical ones and spliting the data into training and testing. We have used 6 different machine learning models here as follows;

* Naive Random Oversampling

  * Balanced Accuracy score - 0.649

<img width="804" alt="Screen Shot 2021-02-14 at 2 51 17 PM" src="https://user-images.githubusercontent.com/71113701/107888780-26eb2980-6ed4-11eb-94f9-9555603931d5.png">










* SMOTE Oversampling

  * Balanced Accuracy score - 0.607

<img width="822" alt="Screen Shot 2021-02-14 at 2 54 32 PM" src="https://user-images.githubusercontent.com/71113701/107888858-9d882700-6ed4-11eb-9ee9-7fb3266dfcf1.png">








 * Undersampling

   * Balanced Accuracy score - 0.5125

<img width="825" alt="Screen Shot 2021-02-14 at 2 57 10 PM" src="https://user-images.githubusercontent.com/71113701/107888978-b3e2b280-6ed5-11eb-8acd-882e31a81752.png">




* Combination (Over and Under) Sampling

  * Balanced Accuracy score - 0.515


<img width="852" alt="Screen Shot 2021-02-14 at 2 57 28 PM" src="https://user-images.githubusercontent.com/71113701/107889003-bfce7480-6ed5-11eb-9303-84ca0b09f6e7.png">



 * Balanced Random Forest Classifier

   * Balanced Accuracy score - 0.787
<img width="821" alt="Screen Shot 2021-02-14 at 3 04 37 PM" src="https://user-images.githubusercontent.com/71113701/107889045-04f2a680-6ed6-11eb-9792-762008f664e8.png">





* Easy Ensemble AdaBoost Classifier

   * Balanced Accuracy score - 0.925




<img width="841" alt="Screen Shot 2021-02-14 at 3 04 44 PM" src="https://user-images.githubusercontent.com/71113701/107889078-1471ef80-6ed6-11eb-9fff-772e62a0ee80.png">

***Summary***

* credit_risk_resampling.ipynb


We used the imbalanced-learn library to resample the data and built and evaluated logistic regression classifiers using the resampled data.We used 4 mode

Naive Random Oversampling

SMOTE Oversampling

Undersample the data using the cluster centroids algorithm.

Use a combination approach with the SMOTEENN algorithm.

For each of the above:


. Train a logistic regression classifier (from Scikit-learn) using the resampled data.

 .Calculate the balanced accuracy score using balanced_accuracy_score from sklearn.metrics.

 .Generate a confusion_matrix.

  .Print the classification report (classification_report_imbalanced from imblearn.metrics).


* credit_risk_ensemble.ipynb

we trained and compared two different ensemble classifiers to predict loan risk and evaluated each model.We used two models

Balanced Random Forest Classifier
Easy Ensemble AdaBoost Classifier

For each of the above:

Train the model and generate predictions.

Calculate the balanced accuracy score.

Generate a confusion matrix.

Print the classification report (classification_report_imbalanced from imblearn.metrics).



 

Balanced Accuracy is the average of sensitivity and specificity with a min = 0 and max = 1. Balanced accuracy is the most accurate the closer its value is to 1. From the 6 machine learning models we worked with in this challenge, Easy Ensemble AdaBoost Classifier has the highest balanced accuracy score at 0.925

 If we look at the f1 score for all 6 models above we will see that the f1 score for Easy Ensemble AdaBoost Classifier is the higest as well at 0.97. f1 score is a weighted harmonic mean of precision and recall such that the best score is 1.0 and the worst is 0.0.

We can therfore recommend using the Easy Ensemble AdaBoost Classifier model for our data.
