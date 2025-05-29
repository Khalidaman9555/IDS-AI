# 🛡️ AI-Driven IDS for IoT/IIoT - Project Overview

## 📁 Project Structure and Execution Flow

This project implements a Federated Learning-based Intrusion Detection System (IDS) for IoT/IIoT environments using simulated sensors, machine learning models (MLP/LSTM), real-time monitoring, and benchmarking.

---

## 🔁 Full Execution Pipeline (Step-by-Step)

### 1. `data_preprocessing.py`
- **Function**: Clean, scale, encode, and prepare the dataset.
- **Output**: Saved preprocessed `.csv` file or dataframe.

### 2. `sensors_and_attacks.py`
- **Function**:
  - Defines multiple realistic sensor types.
  - Simulates normal and attack scenarios (DDoS, SQL Injection, etc).
- **Output**: Real-time simulated sensor readings & attack logs.

### 3. `mlp_lstm.py` and `training.py`
- **Function**:
  - `mlp_lstm.py`: Builds LSTM and MLP models.
  - `training.py`: Trains these models on the preprocessed dataset.
- **Output**: Trained models saved as `.h5` (Keras) or `.pkl` (sklearn).

### 4. `federated_learning_ids.py`
- **Function**: Simulates federated clients each training locally on partitioned datasets.
- **Output**: Updated model weights, performance logs.

### 5. `system_integration_ids.py`
- **Function**:
  - Main controller to run sensor data, attacks, and model predictions together.
  - Integrates simulation, local client predictions, and data routing.
- **Output**: Coordinated simulation logs.

### 6. `dashboard.py`
- **Function**: Visualizes real-time IDS results via Streamlit.
- **Output**: Live GUI showing prediction results, probability, latency, etc.

### 7. `model_comparison_and_benchmarking_for_ids_ai_project_.py`
- **Function**: Benchmark accuracy, F1-score, ROC, latency, etc. across models.
- **Output**: Graphs, saved reports, performance plots.

---

## ⚙️ How to Run the Entire System
```bash
# 1. Preprocess dataset
python data_preprocessing.py

# 2. Generate sensor & attack data
python sensors_and_attacks.py

# 3. Train ML models
python mlp_lstm.py
python training.py

# 4. Federated learning (local + global update)
python federated_learning_ids.py

# 5. Integrate everything (system simulation)
python system_integration_ids.py

# 6. Launch monitoring dashboard (Streamlit)
streamlit run dashboard.py

# 7. Run benchmarking evaluation
python model_comparison_and_benchmarking_for_ids_ai_project_.py
```

---

## 📊 Output Expectations
- **Trained Models**: `models/*.h5` or `*.pkl`
- **Simulated Logs**: `logs/` or `results/`
- **Dashboard UI**: Real-time Streamlit interface
- **Benchmark Results**: Precision, recall, F1-score charts, latency

---

## 🧠 Technologies Used
- Python, Keras, Scikit-learn
- Streamlit (dashboard)
- Pandas, NumPy, Seaborn, Matplotlib
- Simulated IoT attacks and sensors
- Federated Learning logic

---

## 📌 Notes
- This project uses the **Edge-IIoTset** dataset as a core foundation.

