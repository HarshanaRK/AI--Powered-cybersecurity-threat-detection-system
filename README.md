# AI--Powered-cybersecurity-threat-detection-system
Got it! I can help you **rewrite your README** so it matches your **SOC Analyst-focused AI Cybersecurity Threat Detection project**. Here’s a polished version tailored for your project:

---

# AI-Powered Cybersecurity Threat Detection System

This project implements an AI-powered system to detect cybersecurity threats across multiple domains, including **network anomalies, malware, and phishing emails**. The system leverages machine learning models to identify potential threats in test data and can be easily extended for real-world applications.

---

## Features

* **Network Anomaly Detection:** Detects unusual patterns in network traffic using an autoencoder and Isolation Forest.
* **Malware Detection:** Classifies executable files as benign or malicious based on simulated PE file features.
* **Phishing Detection:** Detects phishing emails using text analysis (TF-IDF) and Random Forest.
* **Synthetic Data Generation:** Generates test datasets for training and evaluation.
* **Model Persistence:** Saves trained models for future use without retraining.

---

## Prerequisites

* **Python:** Version 3.8 or higher (tested with Python 3.12)
* **Dependencies:** Install using `requirements.txt`

---

## Installation

1. **Clone the Repository**

```bash
git clone https://github.com/HarshanaRK/AI--Powered-cybersecurity-threat-detection-system.git
cd AI--Powered-cybersecurity-threat-detection-system
```

2. **Set Up a Virtual Environment (Optional)**

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

3. **Install Dependencies**

```bash
pip install -r requirements.txt
```

---

## Usage

1. **Run the Main Script**

```bash
python main.py
```

This script will:

* Train models on synthetic data.
* Test models on sample network, malware, and phishing data.
* Save trained models in `./models`.

2. **Expected Output** (Example)

```
Training Cybersecurity Threat Detection System...
Training Network Anomaly Detection Models...
Training Malware Detection Model...
Training Phishing Detection Model...
===== TESTING THREAT DETECTION SYSTEM =====
1. Network anomalies detected: <number> / 1000 flows
2. Malware detection results: file1.exe → MALWARE (95% confidence)
3. Phishing detection results: Email1 → PHISHING (90% confidence)
All models saved to ./models
```

3. **Custom Usage**

* Replace synthetic data with real datasets by modifying `detector.detect_*` methods in `main.py`.
* Load saved models with `detector.load_models()` for predictions without retraining.

---

## File Structure

```
├── main.py                # Main script
├── models/                # Saved models (auto-created)
│   ├── network_autoencoder.pkl
│   ├── network_isoforest.pkl
│   ├── network_scaler.pkl
│   ├── malware_detector.pkl
│   ├── phishing_vectorizer.pkl
│   └── phishing_detector.pkl
├── requirements.txt       # Dependencies
└── README.md              # This file
```

---

## How It Works

* **Network Anomaly Detection:** Uses an MLPRegressor autoencoder and Isolation Forest to detect anomalies in features like bytes sent/received, duration, port, protocol, and service.
* **Malware Detection:** Random Forest classifier on PE file features (file size, entropy, imports).
* **Phishing Detection:** TF-IDF vectorization and Random Forest classify emails based on text features.
* **Synthetic Data:** Generates reproducible training and testing datasets.

---

## Contributing

* Fix bugs, improve detection, or extend the system with additional datasets.
* Pull requests and issues are welcome.

---

## License

This project is unlicensed. Free to use for educational or personal purposes.

---

**GitHub Repository:**
[https://github.com/HarshanaRK/AI--Powered-cybersecurity-threat-detection-system](https://github.com/HarshanaRK/AI--Powered-cybersecurity-threat-detection-system)

---
