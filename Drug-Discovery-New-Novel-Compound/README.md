# Cheminformatics Project: Predicting Biological Activity of Compounds using Machine Learning

## Project Overview & Focus:

This project aims to develop a machine learning pipeline for predicting the biological activity (pIC50 values) of chemical compounds. The project is rooted in drug discovery, leveraging bioinformatics tools to evaluate compounds for their potential as drug candidates by targeting Acetylcholinesterase, an enzyme relevant in neurological functions.

Using molecular descriptors calculated from chemical compounds, various regression models were built and tested to predict their biological activity. The primary objective of the project is to predict pIC50 values, aiding in the drug discovery process by exploring the relationship between molecular features and biological efficacy.

## Key Steps:

* Part 1: Data Collection and Preprocessing
  - Gathered biological activity data from the ChEMBL database. The dataset contains compounds tested for activity against Acetylcholinesterase.
  - Cleaned and preprocessed the dataset to prepare it for further analysis.
* Part 2: Lipinski Descriptors and Exploratory Data Analysis
  - Calculated Lipinski descriptors to predict the drug-likeness of compounds based on properties such as molecular weight and lipophilicity.
  - Performed exploratory data analysis (EDA) using box plots and scatter plots to highlight differences between active and inactive compounds.
* Part 3: Dataset Preparation and Molecular Descriptor Calculation
  - Computed molecular descriptors using PADEL-Descriptor software.
  - Prepared the dataset for model training, with the molecular descriptors as the input variables (X) and the pIC50 values as the target variable (Y).
* Part 4: Model Building and Evaluation
  - Built and evaluated several regression models, including Linear Regression, Random Forest, AdaBoost, and others, to predict pIC50 values.
  - The Random Forest Regressor showed the best performance on the validation set compared to other models.

**Model Performance:**

Based on the R² score, the Random Forest Regressor achieved the highest score on the validation set among all models. However, when tested on the unseen test set, the accuracy of the model remained relatively low, with an R² score of approximately 0.42. This indicates that the model's ability to predict pIC50 values is still limited, and further model development and selection are necessary to improve its predictive accuracy.

## Tools & Technologies:

- **Python**: For data preprocessing, model building, and evaluation.
- **Scikit-learn**: Used to implement machine learning algorithms and hyperparameter tuning.
- **PADEL-Descriptor**: To calculate molecular descriptors.
- **Matplotlib & Seaborn**: For visualizing data trends during EDA.

## Conclusion:

While the Random Forest Regressor provided the best results on the validation set, the model's performance on the test set was suboptimal. The accuracy of the model, measured by the R² score, was around 0.42, suggesting that the current model struggles to accurately predict pIC50 values. Further refinement of the model, including exploring other algorithms and improving hyperparameter tuning, is necessary to enhance performance.

