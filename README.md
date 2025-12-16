# 💉 H1N1 and Seasonal Flu Vaccines Analytics

## 📝 Overview
Vaccination is a **key public health measure** used to fight infectious diseases. This project analyzes the results of a 2009 US phone survey where respondents were asked about their H1N1 and Seasonal Flu vaccine uptake, alongside questions covering:

* Social, economic, and demographic background.
* Opinions on illness risk and vaccine effectiveness.
* Behaviors towards mitigating transmission.

A better understanding of how these characteristics are associated with personal vaccination patterns provides **guidance for future public health efforts** aimed at healthcare providers/researchers and policymakers.

This file explores the results obtained from building and comparing a **Logistic Regression** model and a **Decision Tree** model to predict vaccine uptake behavior.

---

## 💻 Modeling

### Model Selection
Two classification models were developed to predict vaccine uptake behavior:

1.  **Logistic Regression**
    * A linear model estimating the probability of vaccine acceptance.
    * Selected for its **interpretability** and effectiveness with binary classification.
    * Provides coefficient estimates showing the influence of each predictor.
    * 

2.  **Decision Tree Classifier**
    * A non-linear model creating a tree-like structure of decision rules.
    * Captures non-linear relationships and feature interactions.
    * Provides visual interpretability through the tree structure.
    * 

[Image of a simple Decision Tree diagram]


### Model Training Process
The following steps were performed before model training:

1.  **Data Preprocessing**
    * Handled missing values through imputation or removal.
    * Encoded categorical variables (One-hot encoding for nominal, label encoding for ordinal).
2.  **Feature Engineering**
    * Created interaction terms (e.g., age and chronic conditions).
    * Selected most relevant features based on correlation analysis and domain knowledge.

---

## 📊 Model Comparison

| Feature | Logistic Regression | Decision Tree | Difference |
| :--- | :--- | :--- | :--- |
| **Accuracy** | **86.69%** | 78.00% | **+8.69 percentage points** |
| **Generalization** | Superior (Less Overfitting) | Lower (Potential Overfitting) | Better |
| **Stability** | More stable predictions | Less stable | Better |
| **Conclusion** | **Superior Model** | Suggests need for Ensemble Methods (e.g., Random Forest) | N/A |

### Key Takeaways
* **8.69 percentage point improvement** represents approximately **9 fewer errors per 100 predictions** by the Logistic Regression model.
* The Logistic Regression model's strong performance indicates that vaccine decision-making follows relatively **linear patterns** based on the analyzed demographic and health-related factors.

---

## 📈 Feature Importance
The analysis identified the most influential factors (predictors) of vaccine uptake:

| Rank | Feature | Implication |
| :--- | :--- | :--- |
| **1** | **Doctor Recommendation** | Strongest predictor of vaccination behavior. |
| **2** | **Health Insurance Status** | Access to healthcare increases the likelihood of vaccination. |
| **3** | **Age** | Older individuals are more likely to vaccinate. |
| **4** | **Chronic Medical Conditions** | Existing health concerns drive vaccination compliance. |
| **5** | **Education Level** | Higher education correlates with vaccine acceptance. |

---

## ✅ Model Strengths and Limitations

### Logistic Regression
| Strengths | Limitations |
| :--- | :--- |
| **High Interpretability** - Clear understanding of feature impact. | Assumes **linear relationships** between features and log-odds. |
| **Robust Performance** with 86.69% accuracy. | May miss complex **non-linear patterns**. |
| **Computationally Efficient** for deployment. | Requires careful **feature engineering** for optimal performance. |
| Provides **probability estimates** for predictions. | **13.31% error rate** indicates room for improvement. |

---

## 💡 Conclusion & Practical Applications

This analysis successfully developed a predictive model for vaccine uptake, with **Logistic Regression** as the best-performing model (86.69% accuracy).

### Public Health Implications
The model can **identify individuals at higher risk of non-vaccination**, enabling targeted public health interventions. Healthcare providers play a crucial role, as their recommendations emerged as the top predictor.

### Practical Applications

#### 1. For Public Health Campaigns
* Target outreach to individuals predicted as unlikely to vaccinate.
* Focus resources on populations **without regular healthcare access**.
* **Emphasize the role of healthcare providers** in vaccine promotion.
* Design age-specific messaging strategies.

#### 2. For Healthcare Systems
* Implement prediction tools to **flag patients needing vaccination counseling**.
* Prioritize **doctor-patient conversations** about vaccines during routine visits.
* Allocate resources efficiently based on predicted uptake patterns.

---

## 🛠 Technologies Used
* **Python 3.8+**
* **Pandas**: Data manipulation and analysis
* **NumPy**: Numerical computing
* **Scikit-learn**: Machine learning models and evaluation
* **Matplotlib/Seaborn**: Data visualization
* **Jupyter Notebook**: Interactive development environment

---

## 🙏 Acknowledgments
* Inspired by the DrivenData competition on vaccine prediction.
* Thanks to **Moringa School** for guidance and feedback.