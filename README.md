# 🎓 Student Performance Predictor

A web application that predicts a student's academic performance using **Multiple Linear Regression**, built entirely with HTML, CSS, and JavaScript — no backend, no external libraries. This project was developed as part of my internship assignment.

🔗 **Live Demo:** _[add your GitHub Pages link here]_

---

## 📌 Overview

This app predicts a student's **Final Score (%)** and **Letter Grade (A–F)** based on five academic input features. The entire machine learning pipeline — from data generation to model training to prediction — runs client-side in the browser using pure JavaScript.

---

## ✨ Features

- 🎯 **Live Prediction** — Adjust sliders for study hours, attendance, assignments, previous marks, and class participation to get instant predictions.
- 📊 **Dataset Viewer** — Browse all 500 student records in a searchable table, with a one-click **CSV export**.
- 🤖 **Model Insights** — View the trained regression equation, feature coefficients, and evaluation metrics.
- 📈 **Data Visualizations** — Grade distribution, scatter plots with trend lines, and feature importance charts.
- 💻 **Zero Dependencies** — No frameworks, no APIs, no backend. Just one HTML file.

---

## 🗂️ Dataset

Since no real-world dataset was used, **500 synthetic student records** were generated programmatically using a Gaussian (normal) distribution to mirror realistic academic patterns.

**Features included:**

| Feature | Description | Range |
|---|---|---|
| Study Hours Per Day | Average daily study time | 0–12 hrs |
| Attendance Percentage | Class attendance rate | 40–100% |
| Assignments Completed | Out of 10 assignments | 0–10 |
| Previous Semester Marks | Prior academic performance | 20–100 |
| Class Participation | Participation score | 0–10 |
| **Final Score** (target) | Computed final performance | 0–100 |
| **Grade** (target) | Letter grade derived from score | A / B / C / D / F |

Grade boundaries: **A** (85+), **B** (70–84), **C** (55–69), **D** (40–54), **F** (below 40).

---

## 🤖 Machine Learning Model

**Algorithm:** Multiple Linear Regression

**Training method:** The Normal Equation —

```
θ = (XᵀX)⁻¹ Xᵀy
```

solved directly in JavaScript (no iterative gradient descent needed).

**Preprocessing:** All five features are normalized (zero mean, unit variance) before training so that no single feature dominates due to scale differences.

**Prediction formula:**

```
Final Score = bias + w₁(Study Hours) + w₂(Attendance) + w₃(Assignments)
                    + w₄(Previous Marks) + w₅(Participation)
```

---

## 📐 Evaluation Metrics

| Metric | Purpose |
|---|---|
| **R² Score** | Measures how well the model explains variance in the data (closer to 1 = better fit) |
| **Mean Absolute Error (MAE)** | Average prediction error, in points |
| **Accuracy (±5 tolerance)** | % of predictions within 5 points of the actual score |

These are calculated live from the trained model and displayed in the **Model** tab.

---

## 🛠️ Tech Stack

- **HTML5** — structure
- **CSS3** — styling and responsive layout
- **Vanilla JavaScript** — dataset generation, regression training, prediction logic, and canvas-based charts

No frameworks, no ML libraries, no backend — everything runs in a single browser file.

---

## 🚀 How to Run

1. Clone this repository
2. Open `student-performance-predictor.html` in any modern browser
3. That's it — no installation or server required

---

## 📋 Project Structure

```
student-performance-predictor.html   → Full app (dataset + model + UI + charts)
```

---

## 🔮 Future Improvements

- Replace synthetic dataset with a real-world dataset (e.g. from Kaggle)
- Add a backend to persist predictions and user-submitted data
- Experiment with more advanced models (Decision Trees, Random Forest)
- Add user authentication to track individual student progress over time

---

## 📄 License

This project was built for educational/internship assignment purposes.
