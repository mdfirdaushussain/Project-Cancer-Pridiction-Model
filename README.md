# 🎗️ Breast Cancer Prediction Model

> A machine learning classifier that detects breast cancer as **malignant** or **benign** using cell nucleus features — built with Python and Scikit-learn.

---

## 📌 Overview

Breast cancer is one of the most common cancers worldwide. Early and accurate diagnosis is critical to improving patient outcomes. This project applies **Logistic Regression** to classify tumors based on digitized features of cell nuclei extracted from fine needle aspirate (FNA) images.

The model achieves high accuracy on held-out test data, making it a strong baseline for medical ML applications.

---

## 📊 Dataset

The dataset used is the well-known **Wisconsin Breast Cancer Dataset**, sourced from [YBI Foundation](https://github.com/YBIFoundation/Dataset/raw/main/Cancer.csv).

**Target Variable:**
| Label | Meaning |
|-------|---------|
| `M` | Malignant (cancerous) |
| `B` | Benign (non-cancerous) |

**Features — 10 cell nucleus measurements (30 total with mean, SE, worst):**

| # | Feature | Description |
|---|---------|-------------|
| 1 | Radius | Mean distance from center to perimeter points |
| 2 | Texture | Standard deviation of gray-scale values |
| 3 | Perimeter | Tumor perimeter |
| 4 | Area | Tumor area |
| 5 | Smoothness | Local variation in radius lengths |
| 6 | Compactness | `perimeter² / area - 1.0` |
| 7 | Concavity | Severity of concave contour portions |
| 8 | Concave Points | Number of concave contour portions |
| 9 | Symmetry | Tumor symmetry |
| 10 | Fractal Dimension | Coastline approximation − 1 |

---

## 🧪 Workflow

```
Data Loading → EDA → Feature Selection → Train/Test Split → Model Training → Evaluation
```

1. **Import & Load Data** — Fetch the cancer dataset via URL
2. **Exploratory Data Analysis** — `.head()`, `.info()`, `.describe()`
3. **Define Target & Features** — `y = diagnosis`, `X = all cell nucleus features`
4. **Train/Test Split** — 70% training / 30% testing (`random_state=2529`)
5. **Model Selection** — Logistic Regression (`max_iter=5000`)
6. **Training** — Fit the model on training data
7. **Prediction** — Generate predictions on test set
8. **Evaluation** — Confusion matrix, accuracy score, classification report

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading & manipulation |
| `scikit-learn` | Model building & evaluation |
| `LogisticRegression` | Classification algorithm |

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas scikit-learn jupyter
```

### Run the Notebook
```bash
git clone https://github.com/your-username/cancer-prediction-model.git
cd cancer-prediction-model
jupyter notebook Cancer_pridiction_model.ipynb
```

---

## 📈 Model Performance

The model is evaluated using:

- ✅ **Confusion Matrix** — Visual breakdown of correct vs. incorrect predictions
- ✅ **Accuracy Score** — Overall prediction accuracy
- ✅ **Classification Report** — Precision, Recall, and F1-score per class

> Logistic Regression is well-suited for binary medical classification due to its interpretability and reliable performance on linearly separable data.

---

## 📁 Project Structure

```
cancer-prediction-model/
│
├── Cancer_pridiction_model.ipynb   # Main Jupyter notebook
└── README.md                       # Project documentation
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -m 'Add some improvement'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙏 Acknowledgements

- Dataset sourced from [YBI Foundation](https://github.com/YBIFoundation/Dataset)
- Inspired by the UCI Machine Learning Repository's Breast Cancer Wisconsin dataset

---

<p align="center">Made with ❤️ for better healthcare through data science</p>
