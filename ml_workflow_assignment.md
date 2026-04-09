# ML Workflow Assignment

## Task 1: Label and Data Leakage

**Label Column:** `repeat_purchase_flag`

This is the label because it directly represents the outcome we are trying to predict — whether a customer will make a repeat purchase within 30 days — making it the target variable for our classification model.

**Data Leakage Column:** `discount_used_on_repeat_order`

This column would introduce data leakage because the discount applied on a repeat order only becomes known *after* the repeat purchase has already occurred, meaning this information would not be available at the time of prediction in a real-world scenario.

---

## Task 2: Two Missing ML Workflow Steps

**Step 1 — Exploratory Data Analysis (EDA)**

Before training any model, EDA should be performed to understand the dataset — checking for missing values, outliers, class imbalance in `repeat_purchase_flag`, and correlations between features. Skipping this step risks training a model on flawed or misunderstood data, which leads to unreliable predictions regardless of how powerful the algorithm is.

**Step 2 — Baseline Model**

A simple baseline model (such as Logistic Regression or a Dummy Classifier) should be trained before jumping to gradient boosting. This establishes a performance benchmark so we can objectively measure whether the complex model is genuinely adding value, or simply overfitting the training data without real generalization.
