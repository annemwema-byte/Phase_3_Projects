# H1N1 AND SEASONAL FLU VACCINES ANALYTICS

## Overview
### Vaccination, a key public health measure used to fight infectious diseases. Respondents to a phone survey in the US in 2009, were asked whether they had received the H1N1 and Seasonal Flu vaccines in conjuction with questions about themselves. These additional questions covered their social, economic, and demographic background, opinions on risks of illness and vaccine effectiveness, and behaviours towards mitigating transmission.
### A better understanding of how these characteristics are associated with personal vaccination patterns provide guidance for future public health efforts.
### This file explores the results gotten from building a Logistic Regression model and a Decision Tree model. I will further interpret the results to my stakeholders who are healthcare providers/researchers and policymakers in the health sector.

## Modeling 

### Model Selection
### Two classification models were developed to predict vaccine uptake behavior:
### 1. Logistic Regression
### A linear model that estimates the probability of vaccine acceptance based on weighted combinations of input features. Selected for its interpretability and effectiveness with binary classification problems. Handles categorical variables well after appropriate encoding. Provides coefficient estimates showing the influence of each predictor
### 2. Decision Tree Classifier
### A non-linear model that creates a tree-like structure of decision rules. Splits data based on feature values to classify individuals into vaccinated/non-vaccinated groups. Captures non-linear relationships and feature interactions without explicit specification. Provides visual interpretability through tree structure

### Model Training Process
### 1. Data Preprocessing
### Handled missing values through imputation or removal. Encoded categorical variables (one-hot encoding for nominal features, label encoding for ordinal features).
### 2. Feature Engineering
### Created interaction terms between related features (e.g., age and chronic conditions). Selected most relevant features based on correlation analysis and domain knowledge.

## Model Comparison
### 1. Logistic Regression emerged as the superior model:
### Achieved 86.69% accuracy compared to Decision Tree's 78% 8.69 percentage point improvement represents approximately 9 fewer errors per 100 predictions. Better generalization to unseen data, indicating less overfitting. More stable predictions across different subsets of the data
### 2. Decision Tree Performance:
### Lower accuracy suggests potential overfitting to training data
### May have created overly specific decision rules that don't generalize well. Could benefit from ensemble methods (Random Forest, Gradient Boosting) to improve performance.

## Feature Importance
### 1. Top Predictors of Vaccine Uptake:
### Doctor recommendation is the strongest predictor of vaccination behavior
### Health insurance status - Access to healthcare increases likelihood
### Age (Older individuals are more likely to vaccinate)
### Chronic medical conditions implies health concerns drive vaccination
### Education level shows that Higher education correlates with vaccine acceptance


## Model Strengths and Limitations
### 1. Logistic Regression Strengths:
### High interpretability - clear understanding of feature impact
### Robust performance with 86.69% accuracy
### Computationally efficient for deployment
### Provides probability estimates for predictions.

### 2. Limitations:
### Assumes linear relationships between features and log-odds
### May miss complex non-linear patterns in the data
### Requires careful feature engineering for optimal performance
### 13.31% error rate indicates room for improvement

## Conclusion

### This analysis successfully developed predictive models for H1N1 and seasonal flu vaccine uptake, with Logistic Regression achieving 86.69% accuracy as the best-performing model. The modeling process revealed several insights:
### 1. Predictive Factors:
### The most influential factors in vaccine uptake are doctor recommendations, health insurance coverage, age, and existing chronic conditions. This highlights the importance of healthcare access and provider engagement in vaccination campaigns.
### 2. Model Performance:
### Logistic Regression significantly outperformed the Decision Tree (86.69% vs 78% accuracy), demonstrating that vaccine decision-making follows relatively linear patterns based on demographic and health-related factors rather than complex non-linear interactions.
### 3. Public Health Implications:
### The model can identify individuals at higher risk of non-vaccination, enabling targeted public health interventions. Healthcare providers play a crucial role, as their recommendations emerged as a top predictor of vaccine acceptance.

## Practical Applications
### 1. For Public Health Campaigns:
### Target outreach to individuals predicted as unlikely to vaccinate
### Focus resources on populations without regular healthcare access
### Emphasize the role of healthcare providers in vaccine promotion
### Design age-specific messaging strategies

### 2. For Healthcare Systems:
### Implement prediction tools to flag patients needing vaccination counseling
### Prioritize doctor-patient conversations about vaccines during routine visits
### Allocate resources efficiently based on predicted uptake patterns

## Technologies Used
### 1. Python 3.8+
### 2. Pandas - Data manipulation and analysis
### 3. NumPy - Numerical computing
### 4. Scikit-learn - Machine learning models and evaluation
### Matplotlib/Seaborn - Data visualization
### 5. Jupyter Notebook - Interactive development environment

## Acknowledgments
### Inspired by DrivenData competition on vaccine prediction
### Thanks to 'Moringa School' for guidance and feedback.