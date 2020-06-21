# Credit Risk Application

With the use of supervised machine learning, we use several models to predict credit risk. Some of the main features that helped us determine which model to use were the following:

  1. Accuracy Score
  2. Precision Score
  3. Recall Score
  4. F1 Score
  5. Confusion Matrix
  
## Resources

  - Data Source: LoanStats_2019Q1.csv
  - Software: Python 3.7.6, Jupyter Lab 1.2.6
  - Libraries: Warnings, Numpy, Pandas, Pathlib, Collections, Sklearn, Imblearn
  
## Summary

As we ran each model, we chose to stay consistent with all parameters, such as using the *newton-cg* solver for our Logistic Regression model. 

After comparing the results, we decided to recommend the Naive Random Oversampling model for predicting credit risk.

|Model|Accuracy Score|Precision - high risk|Recall - high risk|F1 - high risk|Precision - low risk|Recall - low risk|F1 - low risk|
|-----|--------------|---------|------|--|-----|--------|-----|
|Naive Random Oversampling| 0.7168| 0.01| 0.72|0.03|1.00|0.71|0.83|
|SMOTE Oversampling|0.6700|0.01|0.57|0.03|1.00|0.77|0.87|
|Undersampling|0.6432|0.01|0.90|0.02|1.00|0.39|0.56|
|Combination Sampling|0.6962|0.01|0.65|0.03|1.00|0.74|0.85|

A Combination of having a higher accuracy score, lower cases of False Negative predictions, and higher scores for precision and recall scores for low risk predictions was the reason why the Naive Random Oversampling model was chosen. 

We took one step further with running two ensemble classifiers to predict credit risk. The results are shown below:

|Model|Accuracy Score|Precision - high risk|Recall - high risk|F1 - high risk|Precision - low risk|Recall - low risk|F1 - low risk|
|-----|--------------|---------|------|--|-----|--------|-----|
|Balanced Random Forest Classifier| 0.7290| 0.02| 0.61|0.04|1.00|0.84|0.91|
|Easy Ensemble AdaBoost Classifier|0.9316|0.09|0.92|0.16|1.00|0.94|0.97|

As we can see, the Easy Ensemble AdaBoost Classifier has higher scores than the Balanced Random Forest Classifier for Accuracy, Recall, Precision, and F1. We recommend using the Easy Ensemble AdaBoost Classifier because of the higher score and the lower cases of False Negative predictions made the model more accurate at predicting credit risk.

## Usage

**Note:** Please ensure you have all the required and updated softwares on your computer.

  1. Download the following files into the same folder for the project.
  
      - LoanStats_2019Q1.csv
      - credit_risk_resampling.ipynb
      - credit_risk_ensemble.ipynb

  2. In your Anaconda prompt, activate your development environment and navigate to the folder holding the above files and run Jupyter Lab or Jupyter Notebook.

  3. You can now run all the cells to see their outputs. If you want to test out the results, you can change the parameters of the Logistic Regression model.
