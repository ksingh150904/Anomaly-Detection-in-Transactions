# Anomaly Detection in Transactions

This project aims to detect anomalies in financial transaction data using machine learning techniques. It identifies suspicious or unusual transaction patterns that could indicate fraud or errors.

---


## 🧠 Algorithms Used

### 1. **Isolation Forest**
- **Why Used**: Isolation Forest is effective for high-dimensional datasets and is specifically designed for anomaly detection. It isolates anomalies instead of profiling normal data points, which makes it efficient and scalable.
- **Strength**: Works well with skewed data distributions and handles outliers naturally.

### 2. **Local Outlier Factor (LOF)**
- **Why Used**: LOF detects anomalies by measuring the local deviation of density relative to neighbors, making it useful in identifying local outliers.
- **Strength**: It considers the density of the local neighborhood, which helps in identifying subtle anomalies.

---

## 🔍 Step-by-Step Process

### 1. **Data Loading**
- Transaction data is loaded from a CSV file or DataFrame.
- Initial exploration is done to understand data distribution and missing values.

### 2. **Preprocessing**
- **Handling Missing Values**: Missing values are imputed or removed as needed.
- **Feature Scaling**: StandardScaler is used to normalize features for distance-based algorithms.
- **Feature Selection/Engineering**: Relevant features such as transaction amount, time, and user behavior metrics are selected or created.

### 3. **Exploratory Data Analysis (EDA)**
- Visualizations (histograms, boxplots) are created to understand distributions.
- Correlation heatmaps help understand relationships between features.

### 4. **Model Training & Evaluation**
- Each algorithm is trained separately on the scaled dataset.
- Performance metrics include:
  - ROC AUC Score
  - Precision, Recall, F1-score (if labels are available)
  - Visualization of anomalies (e.g., scatter plots, time-series plots)

### 5. **Anomaly Detection**
- Each model generates anomaly scores or binary anomaly flags.
- Detected anomalies are compared across models for ensemble insights.
- Visualizations highlight where anomalies occurred.

### 6. **Result Interpretation**
- Anomalous transactions are analyzed to determine patterns (e.g., unusually high amounts, odd times).
- Final results are exported or used for alert generation.

---

## 📦 Requirements

- Python 3.x
- Libraries:
  - `pandas`, `numpy`
  - `matplotlib`, `seaborn`
  - `scikit-learn`

---

## 📁 Output

- A list of potentially fraudulent transactions
- Anomaly score plots and comparisons
- Model evaluation metrics (if labeled data is available)

---

