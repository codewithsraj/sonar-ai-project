# 🚢 SONAR AI Secure Platform

A machine learning web application that detects underwater objects (Rock or Mine) using sonar signal data — built with Python, Scikit-learn, and Gradio.

---

## 📌 Project Overview

This project uses the classic **SONAR dataset** to classify underwater objects as either a **Rock** or a **Mine** based on 60 sonar echo signal readings. The app features a full login/signup system with role-based access control and an admin panel.

---

## ✨ Features

- 🔐 **User Authentication** — Signup & Login system with session-based role management
- 👤 **Role-Based Access**
  - `Admin` → Full access: Prediction, Analytics, Admin Panel, About
  - `User` → Prediction tab only
- 🎯 **Sonar Prediction** — Enter 60 echo signal values to detect Rock or Mine
- 🎲 **Random Fill** — Auto-fills inputs with random sonar values for quick testing
- 📊 **Analytics Dashboard** — Bar chart comparing accuracy of multiple ML models
- ⚙️ **Admin Panel** — View all users, delete users, promote users to Admin
- 🌐 **Gradio Web UI** — Clean, interactive browser-based interface

---

## 🧠 ML Model

| Model | Accuracy |
|---|---|
| Logistic Regression | 78% |
| K-Nearest Neighbors | 86% |
| Support Vector Machine | 91% |
| **Random Forest (Used)** | **~95%+** |

- **Algorithm:** Random Forest Classifier
- **Estimators:** 300 trees
- **Train/Test Split:** 80% / 20% (stratified)
- **Features:** 60 sonar echo frequency bands
- **Target:** `R` (Rock) or `M` (Mine)

---

## 📁 Project Structure

```
sonar-ai-project/
│
├── SONAR_Detector.ipynb       # Main Colab notebook
├── Copy of sonar data.csv     # Dataset (208 samples, 60 features)
└── README.md                  # Project documentation
```

---

## 🚀 Getting Started

### Run on Google Colab

1. Open the notebook in [Google Colab](https://colab.research.google.com/github/codewithsraj/sonar-ai-project/blob/main/SONAR_Detector.ipynb)
2. Upload `Copy of sonar data.csv` to the Colab session
3. Run all cells
4. Click the generated **Gradio public link**

### Install Dependencies (Local)

```bash
pip install gradio pandas scikit-learn matplotlib numpy
```

### Run Locally

```bash
jupyter notebook SONAR_Detector.ipynb
```

---

## 🔑 Default Admin Credentials

| Username | Password | Role |
|---|---|---|
| `admin` | `1234` | Admin |

> ⚠️ Change the default password before deploying publicly.

---

## 🗂️ Dataset Info

- **Source:** UCI Machine Learning Repository — Connectionist Bench (Sonar)
- **Samples:** 208
- **Features:** 60 continuous sonar frequency values (range: 0.0 – 1.0)
- **Classes:** `R` = Rock, `M` = Mine

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.x | Core language |
| Scikit-learn | ML model training |
| Gradio | Web UI |
| Pandas / NumPy | Data handling |
| Matplotlib | Analytics graphs |

---

## 👨‍💻 Author

**Sraj** — [@codewithsraj](https://github.com/codewithsraj)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
