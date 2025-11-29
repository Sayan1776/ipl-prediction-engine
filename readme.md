# IPL Prediction Engine

A machine learning-powered web application that predicts the outcome of IPL matches using historical delivery-level data, matchup stats, and team performance metrics. Built with **Python**, **Flask**, **Pandas**, **NumPy**, and **Scikit-learn**, this project provides match-by-match winner predictions and a full tournament simulation.

---

## 🚀 Features

### 🔮 Match Winner Prediction

Predicts the winning team for any scheduled match using:

* Team strengths based on past seasons
* Run rates, wicket patterns, and phase-wise performance
* Venue impact
* Logistic Regression–based probability outputs

### 🏆 Tournament Simulation

Simulates the entire IPL season:

* Match-by-match prediction
* Updates points table dynamically
* Determines playoff contenders and predicted champion

### 🌐 Clean Web Interface

Developed using **Flask + TailwindCSS**:

* Single match prediction page
* Full schedule prediction page
* Tournament simulation page

---

## 📂 Project Structure

```
IPL_Prediction_Engine/
│
├── app.py                     # Flask backend
├── core.py                    # ML model + prediction logic
├── Match_Info.csv             # Aggregated match-level dataset
├── ipl_2025_deliveries.csv    # Ball-by-ball dataset
├── schedule_2025.csv          # IPL 2025 match schedule
├── requirements.txt           # Python dependencies
│
├── templates/                 # HTML templates
│   ├── index.html
│   ├── single.html
│   └── tournament.html
│
└── static/
    └── tailwind.css           # UI styling
```

---

## 🧠 How the Model Works

The prediction model is built using **Logistic Regression**:

* Extracts features from delivery-level data
* Aggregates team metrics (run rate, wickets, overs performance, etc.)
* Trains a classifier to estimate win probabilities
* Outputs the team with the higher predicted win chance

The logic is encapsulated in `core.py` for easy reuse by the Flask app.

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Sayan1776/ipl-prediction-engine.git
cd ipl-prediction-engine
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Run the Flask App

```bash
python app.py
```

Flask will start on:

```
http://127.0.0.1:5000/
```

---

## 🖥️ Web Pages

### `/` – Home Page

Choose between single match prediction or full tournament simulation.

### `/single` – Single Match Predictor

Predicts winner of any specific scheduled IPL match.

### `/tournament` – Tournament Predictor

Simulates all matches and produces:

* Standings
* Win/Loss predictions
* Final predicted champion

---

## 📊 Data Sources

* **Match_Info.csv** – aggregated stats derived from ball-by-ball data
* **ipl_2025_deliveries.csv** – IPL 2025 ball-by-ball dataset
* **schedule_2025.csv** – upcoming IPL fixtures

These files are used to generate features and support the ML model.

---

## 🤝 Contributing

Feel free to open issues or submit pull requests. Improvements like:

* Better model
* More features
* UI enhancements
  are always welcome.

---

## 📝 License

This project is released under the **MIT License**.

---

## ⭐ Show Support

If you like this project, consider starring the repo 🙌
