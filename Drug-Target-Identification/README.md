# Cheminformatics Project: Identification for Potensial Inhibitors for Tyrosine Kinase Enzym using Machine Learning

## Project Overview:
This project aims to develop a machine learning pipeline for predicting the biological activity (pIC50 values) of chemical compounds. The focus lies in drug discovery, leveraging cheminformatics and bioinformatics techniques to evaluate compounds for their potential as inhibitors of Tyrosine Kinase, an enzyme critical in cancer cell signaling and progression. The goal is to explore the relationship between molecular descriptors and biological activity to identify promising drug candidates.

Using molecular descriptors calculated from chemical compounds, various regression models were built and tested to predict pIC50 values. The project emphasizes understanding the key molecular features influencing bioactivity and identifying limitations in current predictive models for future improvement.

---

## Key Steps:
* Part 1: Data Collection and Preparation
  - Collected biological activity data from the ChEMBL database, focusing on compounds targeting Tyrosine Kinase.
  - The dataset contained 383 compounds, which were cleaned and prepared for analysis. Despite its quality, the dataset size was relatively small, presenting challenges for model generalization.

* Part 2: Exploratory Data Analysis (EDA) and Preprocessing
Conducted a detailed EDA to understand the dataset and identify patterns:
  - Distribution of pIC50 values revealed a slight skew, highlighting the need for preprocessing.
  - Key molecular descriptors, such as logP, numHacceptors, and mw, were strongly correlated with bioactivity.
  - Outliers and extreme values in molecular features were identified, which may impact model performance.
  - Visualized relationships using box plots and scatter plots, showing clear differences between active and inactive compounds.
  - Molecular descriptors were computed using cheminformatics tools and standardized for consistency.
  - Features with high correlation or low relevance were removed to reduce dimensionality and enhance interpretability.
  - The dataset was split into training and test sets, with molecular descriptors as input variables (X) and pIC50 values as the target variable (Y).
    
* Part 3: Model Development and Analysis
  - Built and tested several regression models, including Linear Regression, Decision Tree, Random Forest, and AdaBoost Regressor.
  - Conduct model analysis using feature importance plot and residual plot.

---

**Model Performance:** 
The AdaBoost Regressor was the best-performing model on the training and validation sets, with an R² score of 0.8049 and an RMSE of 1.0175.
However, on the unseen test set, the model’s accuracy was moderate, with an R² of 0.73 and an RMSE of 1.60.
These results suggest that while the model captures the general trends, its ability to generalize could be improved by addressing data limitations and exploring more complex algorithms.

---

## Tools & Technologies:
**Python**: For data preprocessing, feature engineering, and model building.
**Scikit-learn**: To implement machine learning algorithms and conduct hyperparameter tuning.
**Matplotlib & Seaborn**: For data visualization during EDA and residual analysis.
**PADEL-Descriptor**: To calculate molecular descriptors from chemical structures.

---

## Conclusion:
This project successfully demonstrated the potential of machine learning to predict the biological activity of chemical compounds targeting Tyrosine Kinase. While the AdaBoost Regressor provided promising results, limitations such as the small dataset size and challenges in handling outliers need to be addressed.
- Expanding the dataset with more compounds will improve model generalization.
- Advanced algorithms and deeper feature engineering should be explored to enhance predictive accuracy.
- Insights from this project provide a foundation for further research and development in drug discovery targeting Tyrosine Kinase.
- By addressing these limitations, future iterations of the project can yield more robust models and actionable insights to guide experimental drug development.
