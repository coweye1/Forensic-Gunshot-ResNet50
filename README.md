# Deep Learning-based Classification of Gunshot Entrance vs. Exit Wounds

## 🩺 Project Overview
This repository contains a specialized deep learning pipeline designed to differentiate between **Gunshot Entrance and Exit Wounds**. Using transfer learning with the **ResNet50** architecture, this project serves as an AI-driven decision support tool to enhance objectivity and documentation in forensic pathological examinations.

## 📊 Dataset & Attribution
The model was trained and evaluated using the **FDCPUnBGunshotDB**, a high-quality forensic dataset.
* **Source:** [FDCPUnBGunshotDB (University of Brasília)](https://github.com/pedrogarciafreitas/FDCPUnBGunshotDB)
* **Description:** The dataset originates from the Federal District Civil Police (FDCP) and provides critical morphological data for forensic research.
* **Acknowledgement:** Special thanks to **Pedro Garcia Freitas et al.** for providing this valuable resource.

## 🛠️ How to Use (Reproducibility)
To ensure ease of use and reproducibility, I have included a GUI-based preprocessing script.

1. **Download Dataset:** Download the raw repository/zip from [FDCPUnBGunshotDB](https://github.com/pedrogarciafreitas/FDCPUnBGunshotDB).
2. **Run Preprocessing:** Execute `preprocess.py`.
   - A file dialog will appear. Select the downloaded `.zip` file.
   - The script will automatically extract, label, and organize images into `train/val/test` folders (70/15/15 split).
   - Temporary files are automatically cleaned up after processing.
3. **Train/Evaluate:** Use the provided `Forensic_Gunshot_ResNet50.ipynb` in Google Colab or a local Jupyter environment.

## 🚀 Key Technical Features
* **Automated Pipeline:** Custom `preprocess.py` for seamless data restructuring.
* **Architecture:** Transfer learning via **ResNet50** (Pre-trained on ImageNet).
* **Imbalance Handling:** Applied **Weighted Cross-Entropy Loss** to address the 2.8:1 class imbalance.
* **Explainable AI (XAI):** Integrated **Grad-CAM** to visualize pathological features (e.g., abrasion rings) identified by the model.

## 📈 Results and Analysis
### 1. Classification Performance
The model achieved a **92.7% validation accuracy** and a **90.1% test accuracy**.

### 2. Confusion Matrix
![Confusion Matrix](cm.png)

### 3. Model Interpretability (Grad-CAM)
![Grad-CAM](grad_cam.png)
*Visual validation confirms that the AI focuses on wound margins and perilesional skin changes.*

## 🧑‍⚕️ About the Author
**Hee Jae Ryu, MD**
* Pathology Residency Applicant (2026 Match)
* Content Creator at 'CowEye' (1.68M+ Subscribers)
* Primary Interests: Digital Pathology & AI-driven Forensic Science
