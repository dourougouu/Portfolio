My Portfolio WEB Page:
https://dourougouu.github.io/Portfolio/

# AIoT Course — Project 2: Human Gesture Recognition

This is a project from the course **"Artificial Intelligence Algorithms and Applications for the Internet of Things (IoT)"** in the 4th year of CEID.

The goal of the project is to recognize human gestures using IMU sensor data collected from accelerometer and gyroscope sensors. Two different machine learning approaches were implemented:

- Raw Time-Series Classification
- Feature Engineering-Based Classification

---

## 📁 Repository Structure

```text
project/
│
├── data/                     
├── notebooks/
│   ├── aiot_project_time_series.ipynb
│   └── aiot_project_feature_engineering.ipynb
├── figures/                  
├── README.md
└── requirements.txt
```

---

## ⚙️ Setup & Installation

### 💠 Python

The project was developed using Python version **3.11+**.

Required Python libraries:

```powershell
• numpy
• pandas
• scipy
• scikit-learn
• matplotlib
• seaborn
• pymongo
• pyyaml
• jupyterlab
```

Installation:

```bash
pip install numpy pandas scipy scikit-learn matplotlib seaborn pymongo pyyaml jupyterlab
```

---

### 💠 MongoDB Installation

The project uses [MongoDB Community](https://www.mongodb.com/try/download/community), which also includes **MongoDB Compass**.

To start MongoDB:

#### ➡️ Windows

```powershell
net start MongoDB
```

To verify the connection:

```powershell
mongosh
```

---

#### ➡️ macOS / Linux

```bash
mongod --dbpath ~/mongodb-data
```

Then:

```bash
mongosh
```

> Connection can also be performed through **MongoDB Compass** using:
>
> `mongodb://localhost:27017`

---

### 💠 Jupyter Lab Installation

#### ➡️ Windows

Inside VSCode terminal:

```bash
pip install notebook
jupyter notebook
```

---

#### ➡️ macOS

```bash
python3 -m venv aiot_env
source aiot_env/bin/activate
python -m pip install --upgrade pip
python -m pip install jupyterlab pandas numpy scipy scikit-learn matplotlib seaborn pymongo pyyaml
jupyter lab
```

---

## 📊 Data Collection Procedure

Data collection was performed in a controlled indoor environment under consistent experimental conditions. All recordings took place at the same location and approximately the same height level, with participants keeping their elbows resting on a table to reduce unnecessary motion variability and improve measurement consistency.

Each gesture recording lasted 1 minute, followed by a short resting period (~20 seconds) to reduce fatigue effects. The process was repeated 5 times per participant and gesture.

---

## 🏷️ Gesture Annotation

Gesture recordings were manually annotated using predefined labels.

Naming convention example:

```text
msdi1
```

Where:

- **m** → participant initials
- **sd** → scroll down
- **i** → index finger
- **1** → experiment number

---

## 📡 Sensor Configuration

### Gyroscope

- Sampling rate: 100 Hz
- Angular velocity range: ±1000 °/sec

### Accelerometer

- Sampling rate: 100 Hz
- Acceleration range: ±2G

---

## ▶️ Running the Project

### 1️⃣ Start MongoDB

Ensure MongoDB is running locally.

---

### 2️⃣ Open Jupyter Notebook

Open one of the following notebooks:

```text
aiot_project_time_series.ipynb
```

or

```text
aiot_project_feature_engineering.ipynb
```

---

### 3️⃣ Run the Notebook

Execute all cells sequentially:

1. Data loading
2. Data preprocessing
3. Time-series segmentation
4. Feature engineering (Notebook 2)
5. Model training
6. Model evaluation

---

## 🤖 Models Used

### Notebook 1 — Raw Time-Series

- k-Nearest Neighbors (k-NN)
- Support Vector Machine (SVM)
- Convolutional Neural Network (CNN)

### Notebook 2 — Feature Engineering

- Classical Machine Learning classifiers using engineered statistical features

---

## 📈 Evaluation

Model performance was evaluated using:

- Accuracy
- Confusion Matrix
- Classification Report
- Precision / Recall / F1-score

---

## 🧠 Results Summary

The fine-tuned k-NN model achieved the highest performance among the evaluated models for the raw time-series approach, while CNN performance was limited by the relatively small dataset size.

