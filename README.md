# eBay Auction Competitiveness — Bagging & Random Forest

This project applies ensemble learning methods to classify whether an eBay auction becomes competitive. Using decision trees, bagging, and random forests, the analysis compares predictive performance, generalization, and business interpretability.

---

## Project Overview

The goal of this assignment is to predict auction competitiveness using structured listing and seller attributes. The project focuses on:

- Building a baseline decision tree model
- Improving performance using Bagging
- Further improving generalization with Random Forest
- Evaluating models using accuracy, F1-score, and gains/lift charts
- Interpreting feature importance to extract actionable seller insights

The dataset is partitioned into 60% training and 40% validation sets with `random_state = 1`.

---

## Models Compared

### 1. Decision Tree (Baseline)
A single tuned decision tree was used as a baseline classifier.  
- Validation accuracy: **0.8758**
- F1-score: **0.8811**
- Lift at first decile: **1.756**

While the tree performed well, it showed sensitivity to the training data.

---

### 2. Bagging Classifier
Bagging combined multiple decision trees trained on bootstrap samples.  
- Validation accuracy: **0.8872**
- F1-score: **0.8921**
- Lift at first decile: **1.827**

Bagging improved generalization by reducing variance relative to the single tree.

---

### 3. Random Forest
Random Forest extended bagging by adding random feature selection at each split.  
- Validation accuracy: **0.9037**
- F1-score: **0.9091**
- Lift at first decile: **1.827**

Random Forest achieved the best overall performance and showed the strongest generalization.

---

## Model Comparison Summary

Across all three models, performance improved as ensemble complexity increased:

- Decision Tree < Bagging < Random Forest
- Bagging reduced variance compared to a single tree
- Random Forest further reduced correlation between trees and improved accuracy

Based on validation results, **Random Forest is the best model for predicting auction competitiveness**.

---

## Feature Importance & Business Insight

Feature importance from the Random Forest model shows that the strongest predictors of a competitive auction are:

- **ClosePrice**
- **OpenPrice**
- **SellerRating**
- **Currency (EUR)**
- **Category (Toys/Hobbies)**

**Actionable insight:**  
Auctions with reasonable opening prices, strong seller ratings, and favorable categories are more likely to attract competitive bidding.

---

## Tools & Techniques

- Python
- scikit-learn
- Decision Trees
- Bagging
- Random Forest
- GridSearchCV
- Gains & Lift Charts

---

## Key Takeaways

- Ensemble methods significantly improve stability and performance
- Bagging reduces variance compared to a single tree
- Random Forest provides the best balance of accuracy and generalization
- Feature importance helps translate model results into real business decisions

---

## Contact

- **Portfolio:** https://hashimgilani.github.io  
- **LinkedIn:** https://linkedin.com/in/syedhashimgilani  
- **Email:** hashimgilani331@gmail.com  

⭐ Thanks for checking out this ensemble learning project!
