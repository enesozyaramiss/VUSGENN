# VUSGENN

This script merges multiple CSV files containing genetic data, preprocesses the data, trains an XGBoost classifier model, evaluates its performance, and analyzes feature importances.

Merging Genetic Data:

The script starts by defining a function merge_genes to merge genetic data from multiple CSV files into a single DataFrame.
It then merges the specified CSV files (file_list) into one CSV file named Genes_Merge_Data.csv.

![image](https://github.com/enesozyaramiss/VUSGENN/assets/62839938/4796d2d3-1cf5-4af4-b440-adebda25ca60)

Data Preprocessing:

It replaces missing values in the column 'ClinVar Clinical Significance' with 0.
Encodes categorical features using Label Encoding.
Drops unnecessary columns like 'Position' and 'rsIDs'.
Model Training and Evaluation:

Splits the data into training and testing sets using train_test_split.
Initializes an XGBoost classifier model and defines hyperparameters for tuning.
Performs hyperparameter tuning using Grid Search Cross Validation (GridSearchCV).
Trains the XGBoost classifier model with the best hyperparameters.
Evaluates the model's performance on the test set using accuracy, precision, recall, F1 score, and confusion matrix.
Population Stability Index:

Calculates the Population Stability Index (PSI) to measure the stability of the population distribution between the true labels and predictions.
Feature Importance Analysis:

Extracts feature importances from the trained XGBoost model.
Saves the feature importances to an Excel file named feature_importances.xlsx.
Note: Before running this script, ensure that all necessary libraries are installed (pandas, numpy, seaborn, xgboost, statsmodels, matplotlib, sklearn, openpyxl, tqdm, pyodbc) and the file paths are correctly specified.

This script is designed for merging, preprocessing, modeling, and analyzing genetic data, particularly for classification tasks using XGBoost.
