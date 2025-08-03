# 📊 Exploratory Data Analysis (EDA) Summary

## 📁 Dataset Features

The dataset includes the following features:

| Feature                  | Description                                                  |
|--------------------------|--------------------------------------------------------------|
| `fixed acidity`          | Most acids involved with wine or fixed or nonvolatile        |
| `volatile acidity`       | Amount of acetic acid in wine (high levels = unpleasant)     |
| `citric acid`            | Found in small quantities, adds 'freshness' to wines         |
| `residual sugar`         | Amount of sugar remaining after fermentation stops           |
| `chlorides`              | Amount of salt in the wine                                   |
| `free sulfur dioxide`    | Prevents microbial growth                                    |
| `total sulfur dioxide`   | Sum of free and bound sulfur dioxide                         |
| `density`                | Density of wine                                              |
| `pH`                     | How acidic or basic the wine is                              |
| `sulphates`              | Wine additive which contributes to sulfur dioxide levels     |
| `alcohol`                | Alcohol percentage of the wine                               |
| `quality`                | Quality score (3 to 8) given by wine tasters                 |


## 🎯 Target Variable Imbalance

- The target variable `quality` is **imbalanced**:
  - Quality `5`: 577 samples
  - Quality `6`: 535 samples
  - Quality `7`: 167 samples
  - Quality `4`: 53 samples
  - Quality `8`: 17 samples
  - Quality `3`: 10 samples
- This imbalance must be considered during model training to avoid bias.

## ⚠️ Outlier Detection

- **Boxplots** indicate the presence of outliers in:
  - `alcohol`
  - `residual sugar`
  - `sulphates`
- These may affect model performance and require treatment (e.g., clipping, transformation, or removal).

## 🔗 Key Correlations with Quality

| Feature            | Correlation with Quality |
|--------------------|---------------------------|
| Alcohol            | **+0.48**                 |
| Volatile Acidity   | **-0.40**                 |
| Sulphates          | ~+0.25                    |
| Citric Acid        | ~+0.20                    |
| Chlorides          | Very weak negative        |
| Residual Sugar     | Near zero                 |

- **Positive Correlation**: Higher `alcohol` or `sulphates` usually indicates better wine quality.
- **Negative Correlation**: Higher `volatile acidity` often means poorer quality.

## 📈 Visual Findings

- Scatterplots reveal:
  - Wines with **higher alcohol** tend to have **better quality**.
  - **Volatile acidity** is inversely related to quality.
- Boxplots further confirm these trends across different `quality` groups.

## 💡 Feature Insights

- Features like `chlorides`, `residual sugar`, and `free sulfur dioxide` show weak or no correlation and may be dropped or down-weighted during feature selection.

---

## ✅ Conclusion

- The dataset exhibits:
  - **Non-linear relationships**
  - **Outliers**
  - An **imbalanced target variable**
- These characteristics should guide **preprocessing**, **resampling**, and **modeling decisions**.

---

