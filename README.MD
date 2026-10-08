# ❤️ Heart Disease Prediction

A machine learning web application that predicts the risk of heart disease based on a patient's clinical information.

The application is built using **Python, Scikit-learn, Pandas, NumPy, Joblib, and Streamlit**. A trained **Support Vector Machine (SVM)** model is used to make predictions.

---

## 🚀 Features

- Interactive Streamlit web interface
- Heart disease risk prediction
- SVM machine learning model
- Feature scaling using a trained scaler
- Uses the same feature columns as the training dataset
- Simple and beginner-friendly UI
- Can be deployed on Render

---

## 🛠️ Technologies Used

- Python
- Streamlit
- NumPy
- Pandas
- Scikit-learn
- Joblib
- Support Vector Machine (SVM)

---

## 📁 Project Structure

```text
Heart-Disease-Prediction/
│
├── app.py
├── requirements.txt
├── README.md
│
├── heart.csv
├── SVM_heart.pkl
├── scaler.pkl
└── columns.pkl
```

### File Description

| File | Purpose |
|---|---|
| `app.py` | Streamlit application |
| `heart.csv` | Heart disease dataset |
| `SVM_heart.pkl` | Trained SVM model |
| `scaler.pkl` | Trained feature scaler |
| `columns.pkl` | Feature columns used during training |
| `requirements.txt` | Python dependencies |
| `README.md` | Project documentation |

---

# ⚙️ Local Setup

## 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Move into the project:

```bash
cd Heart-Disease-Prediction
```

---

## 2. Create a Virtual Environment

Windows:

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

You should see:

```text
(venv)
```

before your terminal path.

---

## 3. Install Dependencies

Make sure `requirements.txt` is in the same directory as `app.py`.

Then run:

```bash
pip install -r requirements.txt
```

The required packages are:

```text
streamlit
numpy
pandas
scikit-learn
joblib
```

---

# ▶️ Run the Application

Start Streamlit:

```bash
streamlit run app.py
```

The application will normally be available at:

```text
http://localhost:8501
```

Open the URL in your browser.

---

# 🧠 Machine Learning Model

The application uses a trained **Support Vector Machine (SVM)** classifier.

The prediction workflow is:

```text
User Input
    ↓
DataFrame
    ↓
Feature Alignment
    ↓
Feature Scaling
    ↓
SVM Model
    ↓
Prediction
    ↓
Heart Disease Risk
```

The application loads three trained objects:

```python
model = joblib.load("SVM_heart.pkl")
scaler = joblib.load("scaler.pkl")
expected_columns = joblib.load("columns.pkl")
```

---

# 📊 Input Features

The application accepts information such as:

- Age
- Sex
- Chest Pain Type
- Resting Blood Pressure
- Cholesterol
- Fasting Blood Sugar
- Resting ECG
- Maximum Heart Rate
- Exercise-Induced Angina
- Oldpeak
- ST Slope

The input is converted into the same feature structure used during model training before prediction.

---

# 📦