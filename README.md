# Income Prediction Project README

## Business Problem and Stakeholders
The goal of this project is to predict whether an individual's income is above or below a certain threshold. The stakeholders include organizations or individuals who are interested in understanding the factors that influence an individual's income and want to use this prediction for decision-making.

## Data Source
The data for this project was sourced from the [Adult Income Dataset](https://www.kaggle.com/datasets/wenruliu/adult-income-dataset) on Kaggle.

## Data Description
The dataset includes various features such as education level, age, gender, occupation, and more, which are believed to influence an individual's income. The target variable is whether the income is above or below a threshold.

## Analytical Insights
1. Correlation Heatmap:
   - Analyzing the correlation heatmap revealed that education level and age are positively correlated with income, indicating that individuals with higher education levels and older age tend to have higher incomes.
   - ![image](https://github.com/uday-routhu/models/assets/24350354/94c73364-8c23-4851-a0c3-4e5b1bbcb36b)


2. Income Distribution:
   - Visualizing the income distribution showed that a significant portion of individuals have incomes below the threshold, which could impact the model's
   - performance.
   - ![image](https://github.com/uday-routhu/models/assets/24350354/c5ca12dc-5dc5-4eb1-9eb4-9b2be904c193)


## Model Performance
### DecisionTreeClassifier
- Training Data:
  - Accuracy: 1.00
- Test Data:
  - Accuracy: 0.81

### LogisticRegression
- Training Data:
  - Accuracy: 0.85
- Test Data:
  - Accuracy: 0.85

### Model with PCA (Logistic Regression)
- Training Data:
  - Accuracy: 0.83
- Test Data:
  - Accuracy: 0.84

## Model Evaluation
- Based on the accuracy scores, the DecisionTreeClassifier achieves the highest accuracy on the training data, but it has the lowest accuracy on the test data, suggesting potential overfitting. 
- The PCA with DecisionTreeClassifier also shows signs of overfitting, as it performs perfectly on the training data but significantly worse on the test data.
- Among the remaining models, both the GridSearchCV model with DecisionTreeClassifier and the LogisticRegression model have similar accuracy scores on both the training and test data. These two models generalize well and have a balance between precision and recall for both classes.
  
## Which Model
- Given that the primary business goal is likely to have a model that generalizes well to new, unseen data, the production model choice should be based on the balance between performance on the test data and avoiding overfitting. In this case, the LogisticRegression model would be a suitable choice for production.

## Recommendations
1. Feature Importance:
   - Provide stakeholders with insights into the most important features that influence an individual's income. This can help them target specific areas for interventions or improvements.

2. Education Initiatives:
   - Based on the analysis, education level was found to be a significant predictor of income. Stakeholders could consider investing in education initiatives to help individuals improve their education and potentially increase their income.

## Conclusion
This project aimed to predict an individual's income using various features from the Adult Income Dataset. The analysis provided insights into the relationships between features and income, and the predictive models helped in achieving accurate income predictions. The recommendations provided can guide stakeholders in making informed decisions to address income-related challenges.


