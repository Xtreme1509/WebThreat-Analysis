# Cybersecurity Threat Detection using Machine Learning

This project presents a machine learning pipeline for detecting cybersecurity threats based on CloudWatch traffic logs. The main objective is to preprocess and analyze network traffic data and apply classification algorithms to identify potential web-based attacks.

## 📁 Project Overview

The notebook performs the following:

- Loads and cleans network traffic data
- Performs feature engineering (e.g., duration calculation, scaling, and encoding)
- Visualizes relationships using correlation matrices and heatmaps
- Analyzes detection types by country
- Builds and evaluates machine learning models (Random Forest and deep learning using Keras)

## 📊 Dataset

- **Source**: `CloudWatch_Traffic_Web_Attack.csv`
- **Contents**: Network session logs including fields like `src_ip_country_code`, `bytes_in`, `bytes_out`, `creation_time`, `end_time`, and `detection_types`.
- **Objective**: Predict the type of threat based on these features.

## 🧪 Features Engineered

- **Duration (seconds)**: Time difference between session creation and end
- **Standard Scaled Features**: `bytes_in`, `bytes_out`, `duration_seconds`
- **One-hot Encoded Features**: `src_ip_country_code`

## 🛠️ Technologies Used

- **Python** with libraries:
  - `pandas`, `numpy`, `seaborn`, `matplotlib`
  - `scikit-learn`: preprocessing, pipelines, modeling
  - `tensorflow.keras`: deep learning
  - `networkx`: graph analysis (if extended)
- **Visualization**: Correlation heatmaps, stacked bar charts

## 🧠 Machine Learning Models

1. **Random Forest Classifier**
   - Handles both numerical and categorical features
   - Evaluated using accuracy and classification report

2. **Neural Network**
   - Implemented using Keras `Sequential` API
   - Includes dense layers, dropout, and activation functions
   - Trained on scaled and encoded features

## 📈 Visualization Highlights

- **Correlation Matrix Heatmap** to detect feature relationships
- **Stacked Bar Charts** to analyze detection types by country

## 📂 How to Run

1. Clone the repository or download the notebook.
2. Place `CloudWatch_Traffic_Web_Attack.csv` in the same directory.
3. Run the Jupyter notebook step-by-step or use `Run All`.
4. Ensure you have all required Python libraries installed.

```bash
pip install pandas numpy seaborn matplotlib scikit-learn tensorflow
```

## 🧹 Future Improvements

- Include feature selection for dimensionality reduction
- Extend classification to multi-label or anomaly detection
- Deploy model as an API using Flask or FastAPI

## 🔒 Disclaimer

This notebook is for educational and research purposes in cybersecurity threat detection. Data used may be synthetic or anonymized.
