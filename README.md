# -Identifying-Credit-Card-Fraudulent-Transaction-using-Machine-Learning

**Selecting the Credit Card Data:**
The credit card dataset is available on the site https://www.kaggle.com/, a Data Science site containing various open-source data. All the features are not available as the data is confidential, so the feature names are hidden by the names (V1 — V28), and only two features, Time and Amount, are not masked. Detecting whether a transaction is fraudulent or legitimate allows businesses to prevent a tremendous amount of loss due to the laundering of a vast amount of money. Therefore, there should be a mechanism to prohibit such illegal activity, and with the aid of machine learning, it is possible to solve this problem.

**Pre-processing Data:**
Data pre-processing is an important step in all machine learning workflow. Firstly, in this project, the missing values have been checked. However, no missing values have been found. Secondly, the duplicate values have been checked, and the dataset contains duplicate values. The duplicate values are then dropped. The Time represents the difference in seconds between the current and first transaction in the dataset, whereas the Amount denotes the total transaction value. Thus, feature scaling is significant to bring all the values on the same scale. In this study, column transformers have been used, allowing different input columns such as Time and Amount to be transformed independently. The features created by the transformer are concatenated to form a single feature space. (Sklearn.Compose.ColumnTransformer — Scikit-Learn 1.0.1 Documentation, n.d.). 

**Transforming Data:**
Synthetic Minority Over-sampling Technique(SMOTE) is one of the most popular oversampling methods, which creates new instances of the minority class by interpolating existing samples. For each pattern X0, the method chooses one of the k nearest neighbours, which belongs to the fraudulent class and, in this case, k=5. A new pattern z has been made at a random position on the line segment linking the pattern and the chosen neighbour.

**Evaluating the Machine Learning Algorithms Results:**
The performance of the machine learning algorithms is evaluated based on the matrices such as Accuracy, Precision, Recall, and F1 score. Accuracy is the ratio of the number of correct predictions with respect to the entire sample. Precision is the number of correctly categorized transactions as legitimate or fraudulent  (S. Jain, 2019) . Recall defines how well the models detect True Positives. The F1 score combines precision and recall by using harmonic mean.

True Positive (TP) is the number of fraudulent transactions anticipated to be fraudulent in this study. The number of legitimate transactions predicted as fraudulent is known as False Positive (FP). The number of fraudulent transactions estimated as the legitimate transaction is known as False Negative (FN). The number of legitimate transactions anticipated as legitimate is known as True Negative (TN).

**Comparing the Machine Learning Algorithms:**
It has been found that the accuracy is 0.99 in all the three models Random Forest Classifier, XGBoost Classifier, and Decision Tree Classifier, than the baseline method Logistic Regression. The Random forest classifier has higher Precision than the other three models, which means it returns more relevant results than the irrelevant results. Again, Logistic Regression has the highest recall, which means it has a low false-negative rate. The F1 score is the highest for Random Forest Classifier, and thus it reveals it performs better than other models. Therefore, we can conclude that Random Forest Classifier outperforms the different models based on the Accuracy and F1-score. 

