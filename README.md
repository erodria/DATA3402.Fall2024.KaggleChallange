# DATA3402.Fall2024.KaggleChallange
## Predicting Horse Health Using Random Forest

------------------------------------------------------------------------
# Abstract
The objective for this repository is to use medical data to predict health outcomes for horses who have died, been eutheanized or survived. The datasets, via Kaggle Challange, were cleaned and preprocessed to prepare it for analysis. Random forest was used for the machine learning model due to it's robustness to noise and ability to handle non-linear relationships. Accuracy, precision, recal, and F-1 score metrics were calculated using train, validation and test sets. The Random Forest model achieved an accuracy of 81%, demonstrating the effectiveness in preducing equine health outcomes.  

-------------------------------------------------------------------------------------------------------------------
# Method
- Data Understanding:
    - train.csv = (1235 x 29) shape
    - test.csv = (824 x 28) shape (since this is our testing set, there is no outcome column)
    - Numerical features include rectal_temp, pulse, respiratory_rate, etc.
    - Categorical features include surger, age, outcome, etc.
  
- Exploratory Data Analysis:
    - Categorical bar graphs, and numerical histograms.
    - Used heatmap to analyze correlation beween columns.

- Data Preprocessing:
    - Id, hospital_num removed
    - Filled missing values "missing" for categorical data. No missings in numerical data.
    - After EDA, dropped lesion_3, and abdomo_protein due to multicollinearity.
    - Encoded categorical columns.

- Machine Learning:
  - Train-validation-test set split.
  - Implemented random forest.
  - Evaluated the performance metrics.
  - Model improvement using grid search, and another evaluation metric calculation. 


