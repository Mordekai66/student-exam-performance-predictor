# 📚 Student Exam Performance Predictor

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?style=flat-square&logo=scikitlearn)
![Gradio](https://img.shields.io/badge/Gradio-UI-yellow?style=flat-square&logo=gradio)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Views](https://visitor-badge.laobi.icu/badge?page_id=Mordekai66.student-exam-performance-predictor)

Regression pipeline that predicts total student exam scores (Math + Reading + Writing) from demographic and behavioral features. Trains and compares Linear Regression, Decision Tree, and Random Forest regressors, tunes hyperparameters via GridSearchCV, and exposes a Gradio interface for real-time score estimation.

---

## Features

- Feature engineering: combines Math, Reading, and Writing scores into a single `Exam Score` target
- Preprocessing: categorical imputation, `LabelEncoder` per column, `StandardScaler` for numeric features
- Model comparison: Linear Regression vs. Decision Tree vs. Random Forest (MSE, MAE, R²)
- Hyperparameter tuning via `GridSearchCV` with 5-fold cross-validation
- Visualizations: score distribution, study time scatter, parental education box plot, actual vs. predicted scatter
- Interactive Gradio UI for live score prediction

---

## Dataset

File: `Student_Exam_Performance.csv`

| Feature | Type |
|---|---|
| Gender | Categorical — Male, Female |
| Parental Education Level | Categorical — High School, College, Bachelor, Master |
| Lunch Type | Categorical — Standard, Free/Reduced |
| Test Preparation Course | Categorical — Completed, Not Completed |
| Study Time | Numeric |
| Absences | Numeric |
| **Exam Score** | **Target — Math + Reading + Writing (continuous)** |

---

## Setup

```bash
pip install -r requirements.txt
```

Place `Student_Exam_Performance.csv` in the same directory as the notebook, then run all cells.

---

## Gradio Interface

After running the final cell, a local web UI launches. Select demographic inputs from dropdowns, enter study time and absences, and the Random Forest model returns the predicted total exam score.

---

## Project Structure

```
.
├── Student_Exam_Performance.ipynb
├── Student_Exam_Performance.csv
├── LICENSE
├── .gitignore
└── README.md
```

---

## License

MIT — see [LICENSE](LICENSE) for full terms.