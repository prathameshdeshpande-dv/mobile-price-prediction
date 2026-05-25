# 📱 Mobile Price Range Prediction

A machine learning classification project that predicts the price range of mobile phones (low, medium, high, very high) based on hardware specifications. Built using Python and Scikit-learn.

---

## 📌 Problem Statement

With thousands of mobile phones in the market, pricing depends heavily on hardware features like RAM, battery, camera quality, and connectivity. This project builds a multi-class classifier to predict which price range a mobile phone falls into based on its specifications.

---

## 📊 Dataset

- **Source:** Mobile Price Range Dataset (Kaggle)
- **Target variable:** `price_range` — 0 (Low), 1 (Medium), 2 (High), 3 (Very High)
- **Features include:**
  - `battery_power` — battery capacity (mAh)
  - `ram` — RAM in MB (most important feature)
  - `px_height`, `px_width` — screen resolution
  - `mobile_wt` — weight of the phone
  - `int_memory` — internal memory (GB)
  - `camera` — front camera megapixels
  - `pc` — primary camera megapixels
  - `talk_time` — longest battery talk time
  - `four_g`, `three_g`, `wifi`, `bluetooth` — connectivity features
  - `n_cores` — number of processor cores
  - `clock_speed` — processor speed (GHz)

---

## ⚙️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.x | Core programming language |
| Pandas | Data loading and manipulation |
| NumPy | Numerical operations |
| Scikit-learn | ML models, preprocessing, evaluation |
| Matplotlib | Data visualization |
| Seaborn | Statistical plots and heatmaps |

---

## 🔄 Project Workflow

```
Raw Data → EDA → Preprocessing → Model Training → Evaluation → Results
```

### 1. Exploratory Data Analysis (EDA)
- Checked class balance across 4 price categories
- Feature importance analysis — RAM showed highest correlation with price range
- Plotted distributions of battery power, RAM, screen resolution by price category

### 2. Data Preprocessing
- No missing values in dataset
- Applied feature scaling using `StandardScaler`
- Split data into 80% train / 20% test

### 3. Model Building
Trained and compared the following multi-class classifiers:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

### 4. Evaluation Metrics
- **Accuracy**
- **Precision, Recall, F1 Score** (macro average)
- **Confusion Matrix**

---

## 📈 Results

| Model | Accuracy |
|---|---|
| Logistic Regression | ~78% |
| Decision Tree | ~82% |
| Random Forest | ~88% |
| KNN | ~84% |
| SVM | ~96% |

> ✅ **Best model: Support Vector Machine (SVM)** with ~96% accuracy

---

## 📂 Project Structure

```
mobile-price-prediction/
│
├── data/
│   └── mobile_data.csv               # Raw dataset
│
├── notebooks/
│   └── mobile_price_prediction.ipynb # Main Jupyter notebook
│
├── outputs/
│   └── plots/                        # EDA and result visualizations
│
├── requirements.txt                  # Python dependencies
└── README.md
```

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/prathameshdeshpande-dv/mobile-price-prediction.git
cd mobile-price-prediction

# 2. Install dependencies
pip install -r requirements.txt

# 3. Open the notebook
jupyter notebook notebooks/mobile_price_prediction.ipynb
```

---

## 📦 Requirements

```
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```

---

## 🔑 Key Learnings

- RAM is the single most important feature for determining mobile price range
- SVM performed exceptionally well on this dataset due to clear class boundaries in feature space
- Multi-class classification requires macro-averaged metrics for fair evaluation across all price categories
- Battery power and screen resolution are secondary but significant predictors

---

## 👤 Author

**Prathamesh Deshpande**
- 📧 pvdeshpande06@gmail.com
- 💼 [LinkedIn](https://www.linkedin.com/in/prathamesh-deshpande-227862275)
- 💻 [GitHub](https://github.com/prathameshdeshpande-dv)
