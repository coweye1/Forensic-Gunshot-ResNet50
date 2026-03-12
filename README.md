# Deep Learning-based Classification of Gunshot Entrance vs. Exit Wounds

## 🩺 Project Overview
This repository contains a specialized deep learning pipeline designed to differentiate between **Gunshot Entrance and Exit Wounds**. Using transfer learning with the **ResNet50** architecture, this project serves as an AI-driven decision support tool to enhance objectivity and documentation in forensic pathological examinations.

## 📊 Dataset & Attribution
The model was trained and evaluated using the **FDCPUnBGunshotDB**, a high-quality forensic dataset.
* **Source:** [FDCPUnBGunshotDB (University of Brasília)](https://github.com/pedrogarciafreitas/FDCPUnBGunshotDB)
* **Description:** The dataset originates from the Federal District Civil Police (FDCP) and provides critical morphological data for forensic research.
* **Acknowledgement:** Special thanks to **Pedro Garcia Freitas et al.** for providing this valuable resource to the academic community.

## 🚀 Key Technical Features
* **Architecture:** Transfer learning via **ResNet50** (Pre-trained on ImageNet) to leverage complex visual feature extraction.
* **Class Imbalance Mitigation:** Applied **Weighted Cross-Entropy Loss** to address the data imbalance (1,883 Entrance vs. 671 Exit wounds), prioritizing the detection of the minority class (Exit wounds).
* **Optimization:** Fine-tuned using the Adam optimizer with a learning rate scheduler for stable convergence.
* **Explainable AI (XAI):** Integrated **Grad-CAM** (Gradient-weighted Class Activation Mapping) to visualize and validate the pathological features (e.g., abrasion rings, margin characteristics) identified by the model.

## 📈 Results and Analysis
### 1. Classification Performance
The model achieved a **92.7% validation accuracy** and a **90.1% test accuracy**. 

### 2. Confusion Matrix
![Confusion Matrix](cm.png)
*The model demonstrates high sensitivity (95%) in identifying entrance wounds, which is crucial for forensic reconstruction.*

### 3. Model Interpretability (Grad-CAM)
![Grad-CAM](grad_cam.png)
*Visual validation confirms that the AI focuses on wound margins and perilesional skin changes, aligning with established forensic diagnostic criteria.*

## 🧑‍⚕️ About the Author
**Hee Jae Ryu (CowEye)**
* MD / Pathology Residency Applicant (2026 Match)
* Digital Media Expert (1.68M Subscribers)
* Research Interests: Digital Pathology, AI-driven Forensic Diagnostics, and Medical Image Analysis.

---
*Disclaimer: This project is for research and educational purposes only and should not be used as a primary diagnostic tool in clinical or legal settings.*
