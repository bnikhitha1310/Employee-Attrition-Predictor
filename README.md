# 👔 Employee Attrition Predictor

A machine learning web app built with **Streamlit** and **scikit-learn** that predicts whether an employee is likely to leave a company based on key HR metrics.

---

## 🚀 Features

- **Exploratory Analysis** — View the preprocessed dataset and a correlation heatmap of all features
- **Logistic Regression Model** — Trained on HR data with accuracy and ROC-AUC metrics displayed
- **Confusion Matrix** — Visual breakdown of true/false positives and negatives
- **Interactive Prediction** — Input an employee's profile via sliders and get an instant attrition prediction

---

## 🖥️ Demo

![Streamlit App](https://img.shields.io/badge/Built%20with-Streamlit-FF4B4B?logo=streamlit&logoColor=white)

---

## 📦 Installation

**1. Clone the repository**
```bash
git clone https://github.com/your-username/employee-attrition-predictor.git
cd employee-attrition-predictor
```

**2. Create a virtual environment (recommended)**
```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Run the app**
```bash
streamlit run app.py
```

---

## 🧰 Requirements

```
streamlit
pandas
numpy
matplotlib
scikit-learn
```

Or install directly:
```bash
pip install streamlit pandas numpy matplotlib scikit-learn
```

---

## 📊 Features Used in the Model

| Feature | Description |
|---|---|
| `Age` | Employee age |
| `YearsAtCompany` | Tenure in years |
| `MonthlySalary` | Monthly salary (₹) |
| `JobSatisfaction` | Satisfaction rating (1–4) |
| `WorkLifeBalance` | Work-life balance rating (1–4) |
| `OverTime` | Whether employee works overtime (0/1) |
| `NumProjects` | Number of active projects |
| `TrainingLastYear` | Training sessions attended last year |
| `SalaryPerYear` | Derived: MonthlySalary × 12 |
| `SatisfactionScore` | Derived: avg of Job + WLB satisfaction |
| `BurnoutRisk` | Derived: OverTime × Projects / (Tenure + 1) |

---

## 🧠 How It Works

1. Raw features are **engineered** to add `SalaryPerYear`, `SatisfactionScore`, and `BurnoutRisk`
2. All features are **standardized** using `StandardScaler`
3. A **Logistic Regression** model is trained on an 80/20 train-test split
4. The app reports **Accuracy** and **ROC-AUC** score on the test set
5. Users can input custom employee data and get a live **Stay / Leave** prediction

---

## 📁 Project Structure

```
employee-attrition-predictor/
│
├── app.py               # Main Streamlit application
├── requirements.txt     # Python dependencies
└── README.md            # Project documentation
```

---

## 📌 Notes

- The current dataset is a small built-in sample (40 records) intended for demonstration. For production use, replace it with a real HR dataset such as the [IBM HR Analytics dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) from Kaggle.
- Model performance metrics will improve significantly with a larger, real-world dataset.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙌 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.