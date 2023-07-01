# credit-card-fraud-detection
Credit card firms must detect fraudulent credit card transactions to prevent consumers from being charged for products they did not buy. Data Science can address such a challenge, and its significance, coupled with Machine Learning, cannot be emphasized.

We will be using the Credit Card Fraud Detection Dataset from Kaggle. The dataset utilized covers credit card transactions done by European cardholders in September 2013. This dataset contains 492 frauds out of 284,807 transactions over two days. The dataset is unbalanced, with the positive class (frauds) accounting for 0.172 percent of all transactions.

Conclusion
This trained different classifiers and performed undersampling and oversampling techniques after splitting the data into training and test sets to decide which classifier is more effective in detecting fraudulent transactions.

GridSearchCV takes a lot of time and is therefore only effective in undersampling since undersampling does not take much time during training. If you find it's taking forever on a particular model, consider reducing the parameters you've passed, and use RandomizedSearchCV for that (i.e., setting is_grid_search to False on our core function).

If you see that searching for optimal parameters takes time (and it does), consider directly using the RandomForestClassifier model, as it's relatively faster to train and usually does not overfit or underfit, as you saw earlier in the tutorial.

The SMOTE algorithm creates new synthetic points from the minority class to achieve a quantitative balance with the majority class. Although SMOTE may be more accurate than random undersampling, it does not delete any rows but will spend more time on training.

It will help if you do not oversample or undersample your data before cross-validation because you are directly impacting the validation set by oversampling or undersampling before using cross-validation, resulting in the data leakage issue.
