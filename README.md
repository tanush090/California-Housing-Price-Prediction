# 🏡 California Housing Price Prediction

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="Scikit-learn"/>
  <img src="https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white" alt="Google Colab"/>
</p>

## 📌 About the Project

This project focuses on predicting California housing prices using machine learning regression algorithms. It explores the dataset, builds a baseline model, compares its performance with Gradient Boosting, and improves predictions through hyperparameter tuning.

The project also includes error analysis and an interactive, user-input-based inference cell for estimating house prices.

## 🎯 Objectives

- Explore and analyze the California Housing dataset.
- Build a baseline Linear Regression model.
- Compare regression model performance.
- Optimize model parameters using `GridSearchCV`.
- Evaluate predictions using standard regression metrics.
- Predict house prices from user-provided features.

## 📊 Dataset

- **Source:** Scikit-learn California Housing dataset
- **Total records:** 20,640
- **Input features:** 8
- **Target:** Median house value
- **Target unit:** $100,000

### Features Used

`MedInc`, `HouseAge`, `AveRooms`, `AveBedrms`, `Population`, `AveOccup`, `Latitude`, `Longitude`

## ⚙️ Workflow

1. **Data Loading** — Load the dataset using Scikit-learn.
2. **Exploratory Data Analysis** — Inspect dataset information, missing values, and statistical summaries.
3. **Data Preparation** — Separate features and target, then split the data into training and testing sets.
4. **Baseline Model** — Train and evaluate Linear Regression.
5. **Model Comparison** — Train `HistGradientBoostingRegressor` and compare results.
6. **Hyperparameter Tuning** — Use `GridSearchCV` to find better model parameters.
7. **Evaluation** — Analyze MAE, RMSE, R² score, and prediction errors.
8. **Inference** — Accept user inputs and generate an estimated house price.

## 🤖 Models Implemented

- **Linear Regression** — Baseline regression model.
- **HistGradientBoostingRegressor** — Nonlinear ensemble regression model.
- **GridSearchCV** — Cross-validated hyperparameter tuning for the Gradient Boosting model.

## 📈 Model Performance

| Metric | Linear Regression | Tuned Gradient Boosting |
|---|---:|---:|
| MAE | 0.533 | 0.294 |
| RMSE | 0.746 | 0.449 |
| R² Score | 0.576 | 0.846 |

*Results are from the notebook's test-set evaluation. Lower MAE and RMSE are better; a higher R² score indicates a better fit.*

### 🏆 Best Model Parameters

```python
{
    "learning_rate": 0.05,
    "max_iter": 300,
    "max_leaf_nodes": 50,
    "l2_regularization": 0
}
```

The tuned Gradient Boosting model achieved an **R² score of approximately 84.62%** on the test set, outperforming the Linear Regression baseline.

## 🛠️ Tech Stack

- **Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib
- **Machine Learning:** Scikit-learn
- **Environment:** Google Colab / Jupyter Notebook

## 📂 Repository Structure

```text
California-Housing-Price-Prediction/
│
├── california_houses.ipynb
├── requirements.txt
└── README.md
```

## 🚀 How to Run

1. Open `california_houses.ipynb` in Google Colab.
2. Run the notebook cells from top to bottom.
3. Review the model comparison and evaluation results.
4. Run the final inference cell and enter housing feature values to obtain a price estimate.

To install dependencies in a local Python environment:

```bash
pip install -r requirements.txt
```

## 🔮 Future Improvements

- Experiment with additional regression algorithms.
- Apply feature engineering and cross-validation.
- Visualize feature importance and prediction errors.
- Deploy the trained model through a simple web application.

## 👨‍💻 Author

**Tanush Kumar**

B.Tech CSE (AI & ML) | Aspiring Machine Learning Engineer

- GitHub: [@tanush090](https://github.com/tanush090)

---

⭐ If you find this project useful, consider giving the repository a star.

*This project is for educational purposes. Predictions are estimates based on the dataset, whose target values are capped near $500,000; they should not be treated as actual property valuations.*
