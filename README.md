# BREAST-CANCER-GENE-EXPRESSION-
Machine learning project analyzing breast cancer gene expression data to classify cancer subtypes, focusing on sampling bias, class imbalance, and model fairness using Logistic Regression and advanced models.
# Breast Cancer Gene Expression Classification

## Business Problem
Breast cancer subtype classification is critical for determining treatment and improving survival rates. However, gene expression datasets are highly dimensional and imbalanced, which can lead to biased or unreliable model predictions.

## Project Overview
This project analyzes gene expression data to classify breast cancer subtypes. It focuses on how sampling strategies and class imbalance affect model performance and fairness.

## Data
- Source: CuMiDa Breast Cancer Dataset (Kaggle)
- Link: https://www.kaggle.com/datasets/brunogrisci/breast-cancer-gene-expression-cumida
- 151 samples  
- 54,676 gene features  
- Multiple cancer subtypes  

## Data Preprocessing
- Train/test split before scaling
- PCA for dimensionality reduction
- Label encoding

## Modeling
- Logistic Regression (best model)
- Random Forest
- XGBoost
- ANN / CNN
## Exploratory data analysis
<img width="309" height="299" alt="image" src="https://github.com/user-attachments/assets/cc5552ba-3e8f-422d-b38b-4c1035ebc740" />
<img width="488" height="388" alt="image" src="https://github.com/user-attachments/assets/caa3cb4d-2b6a-46b0-b099-a4ddec066388" />
Key observations:
- Dataset is highly imbalanced  
- High dimensionality required PCA  
- Gene features show low correlation, increasing modeling complexity  


## Results
- Logistic Regression performed best
- CNN slightly better than ANN in recall
-After removing the validation set, the
Weighted Logistic Regression
improved significantly to 98%.
XgBoost aslo improved but a little
points off Log Regression.​
-SVM (Support Vector Machine) did
incredibly well, but Log
Regression outperformed it after cross
validation and hyper parameter
tunning. 

## Key Insights
- Sampling order affects performance
- Class imbalance skews accuracy
- Stratified sampling improves fairness
### Model Comparison

| Model                | Accuracy | Recall | F1 Score |
|---------------------|----------|--------|----------|
| Logistic Regression | Best     | High   | Strong   |
| Random Forest       | Moderate | Lower  | Moderate |
| XGBoost             | Moderate | Lower  | Moderate |
| ANN                 | Good     | Medium | Good     |
| CNN                 | Slightly better than ANN | High | Strong |
## Model Interpretation

Principal Component Analysis (PCA) was used to reduce dimensionality and identify the most influential feature combinations in the dataset. The first few principal components explained the majority of the variance, indicating that a subset of transformed features drives most of the model's predictive power.

Feature importance analysis shows that certain gene expression patterns contribute more significantly to classification decisions. Logistic Regression provided interpretability by allowing us to understand how these transformed features influenced predictions.

This interpretability is critical in a medical context, where understanding why a prediction is made is just as important as the prediction itself.
## Conclusion
Logistic Regression proved to be the most stable model for this dataset.
## How to Run

1. Clone the repository  
2. Install dependencies:
   pip install -r requirements.txt  

3. Open the notebook in /notebooks  
4. Run all cells to:
   - preprocess the data  
   - train models  
   - evaluate performance  
## Repository Structure

- data/ → contains dataset or sample data  
- notebooks/ → Jupyter notebooks with full analysis and modeling  
- images/ → visualizations used in the project  
- results/ → model outputs and evaluation results  
- models/ → saved models (if applicable)  
- README.md → project documentation  
- requirements.txt → dependencies needed to run the project  

## Deployment
The model was deployed as a decision-support tool for breast cancer risk classification. The application allows users to input gene expression data and receive a predicted cancer subtype along with a confidence score.

Due to access limitations, the live demo link is not publicly available, but the deployment demonstrates the practical application of the model in a clinical decision-support context.
