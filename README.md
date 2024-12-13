# DATA3402.Fall2024.KaggleChallange

## Predicting Horse Health Using Random Forest
This repository contains an attempt to apply Random Forets to Predicting Horse Health using data form the "Predict Health Outcome" from a Kaggle Challange. 
https://www.kaggle.com/competitions/playground-series-s3e22/data?select=train.csv

------------------------------------------------------------------------
# Abstract
The objective for this repository is to use medical data to predict health outcomes for horses who have died, been eutheanized or survived. The datasets, via Kaggle Challange, were cleaned and preprocessed to prepare it for analysis. Random forest was used for the machine learning model due to it's robustness to noise and ability to handle non-linear relationships. Accuracy, precision, recal, and F-1 score metrics were calculated using train, validation and test sets to see our model's performance. The Random Forest model achieved an accuracy of 81%, demonstrating the effectiveness in preducing equine health outcomes. 

-------------------------------------------------------------------------------------------------------------------
# Methods

- Data:
    - train.csv = (1235 x 29) shape
    - test.csv = (824 x 28) shape (since this is our testing set, there is no outcome column)
    - Features
        - Numerical features include rectal_temp, pulse, respiratory_rate, etc.
        - Categorical features include surger, age, outcome, etc.
    - 70% Training, 15% Validation, 15%, Testing

- Data Preprocessing:
    - Removed irrelevant columns such as id, hospital_num.
    - Filled missing values "missing" for categorical data. No missings in numerical data.
    - After EDA, dropped lesion_3, and abdomo_protein due to multicollinearity.
    - Encoded categorical columns for the model.

  
- Exploratory Data Analysis / Visualization:
    - Categorical bar graphs, and numerical histograms.
    - Used heatmap to analyze correlation beween columns.


- Machine Learning:
  - Implemented Random Forest with the following steps: 
      - Train-validation-test set split.
      - Implemented random forest, and tuned hyperparameters using grid search:
          - Evaluated the performance metrics.
      - Evaluated model performance using metrics such as accuracy, precision, recal and F1-score.
 
-----------------------------------------------------------------------------------------------------------------------
# Results
Achieved an accuracy of 81% on the test set, demonstrating the effectiveness of the Random Forest model in predicting equine health outcomes. 

---------------------------------------------------------------------------------------------------------------------

# Conclusion
The project confirmed the Random Forest model's relevance for this task, which balanced bias and variance without overfitting. The optimal hyperparameters improved the model's performance by about 10%.

# Future Work
- Investigate moderate correlations between additional features.
- Explore relationships between hospitals and health outcomes for deeper patterns.



