# Automotive Edge AI & Machine Learning Portfolio 🏎️⚡

**Bridging Classical Systems Engineering with the Modern AI/ML Stack**

This repository contains a complete, hardware-aware Machine Learning pipeline designed for automotive embedded systems. It demonstrates the full MLOps lifecycle: from raw sensor data ingestion and classical predictive maintenance, to Deep Neural Network (DNN) calibration and sub-millisecond edge deployment.

---

## 🏗️ System Architecture & MLOps Pipeline

1. **Data Engineering:** Automated ingestion, imputation, and signal processing of high-frequency time-series sensor data.
2. **Classical ML (Safety-Critical):** Threshold-tuned classification models optimizing for Recall over Precision to prevent catastrophic hardware failures.
3. **Representation Learning:** PyTorch Deep Neural Networks designed to approximate highly non-linear physical system behaviors (e.g., Battery state physics).
4. **Edge Deployment:** Exporting heavy Python architectures into optimized ONNX C++ graphs for sub-millisecond microcontroller execution.

---

## 📂 Project Modules

### Module 1: Sensor Data Pipeline (`day1_data_engineering.ipynb`)
* **Objective:** Replace manual CANape/MDA calibration analysis with automated Python pipelines.
* **Techniques:** Vectorized mathematics for calculated signals (Power from V & I), rolling average low-pass digital filters for sensor noise, and linear interpolation for dropped CAN frames.

### Module 2: Predictive Maintenance & Functional Safety (`day2_predictive_maintenance.ipynb`)
* **Objective:** Predict impending motor failures using multi-sensor matrices (Temperature & Vibration).
* **Techniques:** Scikit-Learn `RandomForestClassifier`, Train/Test splits to prevent data leakage.
* **Engineering Focus:** Tuned the probability safety threshold down to 1% to eliminate False Negatives (missed failures), proving an understanding of ASIL/Functional Safety requirements over raw academic accuracy.

### Module 3: Deep Learning for Battery SoC (`day3_pytorch_soc.ipynb`)
* **Objective:** Calibrate an artificial Neural Network to learn the non-linear physics of a high-voltage battery pack.
* **Techniques:** Built a custom PyTorch Multi-Layer Perceptron (MLP) with ReLU activations.
* **Engineering Focus:** Implemented Mean Squared Error (MSE) loss and an Adam optimizer. Performed Hyperparameter tuning (Learning Rate and Epoch adjustments) to drop absolute prediction error down to 0.02%.

### Module 4: Sub-Millisecond Edge Inference (`day4_onnx_deployment.ipynb`)
* **Objective:** Bridge the gap between Data Science and Firmware Engineering by deploying the Python model to C++.
* **Techniques:** ONNX Tracing, ONNX Runtime (`onnxruntime`), NumPy strict-type arrays.
* **Engineering Focus:** Benchmarked the frozen model's execution time, achieving sub-millisecond inference speeds suitable for high-frequency (100Hz+) embedded control loops.