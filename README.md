# 🖥️ Anomaly Detection in Server Computers

This project focuses on identifying **anomalies in server performance** using statistical methods. It analyzes server data — specifically **throughput** (in MB/s) and **latency** (in ms) — to detect when a server is behaving unusually.

---

## 💡 What Problem Does It Solve?

Servers can sometimes slow down or behave erratically due to hardware issues, traffic spikes, or misconfigurations. Detecting these **anomalies early** can help prevent:
- System failures
- Poor user experiences
- Increased operational costs

This project provides a simple yet effective method for **automated anomaly detection**.

---

## ⚙️ How It Works (High-Level Overview)

1. **Dataset Input**: The dataset includes records of throughput and latency for multiple server computers.
2. **Statistical Modeling**: I fit the dataset into a **Gaussian (normal) distribution**, which helps define what “normal behavior” looks like.
3. **Probability Scoring**: Each data point is assigned a probability of how likely it is under the Gaussian model.
4. **Threshold Selection**:
   - I repeatedly sample threshold values between the **minimum and maximum probabilities**.
   - For each threshold, I calculate the **F1 score**, which balances precision and recall.
   - The threshold with the highest F1 score is selected as the best cut-off for detecting anomalies.
5. **Anomaly Detection**: Any server behavior with a probability lower than the selected threshold is flagged as an anomaly.

---

## 🚀 Getting Started

Follow these steps to set up and run this project on your local machine.

### 📁 Prerequisites

- Python 3.x installed
- `pip` (Python package manager)

---

### ⚙️ Step-by-Step Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/AryaHaldankar/Anomaly-Detection-for-Server-Computers/.git
   cd Anomaly-Detection-for-Server-Computers

2. **Create a virtual environment**
   ```bash
   python -m venv venv

3. **Activate the Virtual Environment**  
   ***- On Wndows***
   ```bash
   venv\Scripts\activate
   ```  
  ***- On Mac/Linux***
  ```bash
  source venv/bin/activate
  ```
4. **Install Project Dependencies**
   ```bash
   pip install -r requirements.txt
   
5. **Add the `data/` Folder**

   Download the `data` folder from the provided link [Drive Link](https://drive.google.com/drive/folders/10VLLqmoMUGGbMM590s9thchlIkT7ps0e?usp=sharing).

   Place the entire `data/` folder inside the root of the project directory — the same directory where your scripts and `requirements.txt` are located.
6. **Run Script**
   ```bash
   python3 programming_exercise_8_anomaly_detection.py
