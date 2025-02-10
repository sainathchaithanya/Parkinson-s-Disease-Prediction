# 🧠 Parkinson's Disease Prediction  

## 📌 Project Overview  
This project focuses on predicting **Parkinson’s disease severity** at different time points (**0, 6, 12, and 24 months**) using **machine learning techniques**. By integrating **biomarker, clinical, and gait data**, this model aims to improve early diagnosis and disease progression monitoring.

---

## 📊 Datasets Used  
The dataset integrates **cerebrospinal fluid (CSF) mass spectrometry (CSF-MS) readings**, **clinical assessments (UPDRS scores)**, and **gait analysis** to provide a multi-modal evaluation of Parkinson’s disease progression.  

### **1️⃣ Protein Dataset**  
- **Source:** [UniProt](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2238893/), [NPX Metrics](https://olink.com/knowledge/faq?query=npx), & [AMP Parkinson’s Dataset (Kaggle)](https://www.kaggle.com/competitions/amp-parkinsons-disease-progression-prediction/data)  
- **Description:** Contains protein expression levels (UniProtKB, UniRef, UniParc).  
- **Relevance:** Helps track **neurodegenerative biomarkers**, including **alpha-synuclein levels**.  

### **2️⃣ Peptides Dataset**  
- **Source:** CSF-MS Peptide Data & [AMP Parkinson’s Dataset (Kaggle)](https://www.kaggle.com/competitions/amp-parkinsons-disease-progression-prediction/data)  
- **Description:** Contains peptide concentrations measured via **mass spectrometry**.  
- **Relevance:** Captures protein breakdown and **biological markers of neurodegeneration**.  

### **3️⃣ Clinical Dataset**  
- **Source:** [MDS-UPDRS Scores](https://www.apta.org/patient-care/evidence-based-practice-resources/test-measures/unified-parkinsons-disease-rating-scale-updrs-movement-disorders-society-mds-modified-unified-parkinsons-disease-rating-scale-mds-updrs) & [AMP Parkinson’s Dataset (Kaggle)](https://www.kaggle.com/competitions/amp-parkinsons-disease-progression-prediction/data)  
- **Description:** Includes **227 proteins, 971 peptides, and UPDRS assessments** at multiple time points.  
- **Relevance:** Provides clinical disease severity scores (**UPDRS I–IV**).  

### **4️⃣ Gait Dataset & Clinical Integration**  
- **Source (Raw Gait Data):** [Gait Data](https://doi.org/10.17632/4tjd8jrhp8.1)  
- **Source (Updated Clinical Dataset with Gait):** [Updated Clinical Dataset with Gait](https://drive.google.com/file/d/1xk9U0-ovwb2QZgNK75IwrLGZZxTUMYr6/view)  
- **Description:** Contains motor function metrics such as gait speed, freezing episodes, stride variability, and balance parameters.  
- **Relevance:** Enhances **motor function assessment** for Parkinson’s disease severity prediction.  

### **5️⃣ Integration of UniProt Protein Dataset with Clinical Data**  
- **Source:** [Final Resultant Dataset](https://drive.google.com/file/d/1xU8p4Y2IdI3xy9V5FnLMEOKzdHfIS14z/view?usp=drivesdk)  
- **Description:** Integrated dataset combining **protein, peptide, and clinical data** for comprehensive analysis.  
- **Relevance:** Enables robust **multi-modal modeling of Parkinson’s disease progression**.  

---

## **🛠️ Model Implementation**  

### **1️⃣ Machine Learning Models**  
The dataset was split **(80:20)** into **training & validation** sets. Several machine learning models were tested, including:  

- **TensorFlow Decision Forests (TFDF)** – Handles **non-linear data** efficiently.  
- **Random Forest Regressor** – Robust ensemble model for structured data.  
- **Linear Regression & KNN** – Baseline models for comparison.  
- **Custom Model (Phase Shift Ensembling)** – Integrates multiple models to **capture disease progression trends**.  

### **2️⃣ Training & Validation Process**  
- **Feature Engineering:** Extracted biomarkers, gait metrics, and clinical scores.  
- **Model Training:** Models optimized using **GridSearchCV for hyperparameter tuning**.  
- **Validation Metrics:** Evaluated using **MSE, sMAPE, and Acceptable Prediction Range (APR)**.  

### **3️⃣ Phase Shift Ensembling & Time-Series Comparisons**  
- Used **Phase Shift Ensembling** to adjust predictions over time.  
- Compared with **LSTMs, RNNs, and Transformers** for sequential modeling.  

### **4️⃣ Final Model Optimization**  
- Developed **Model_Optim_Median** with a **custom loss function** to enhance predictive accuracy.  
- Employed **Stratified K-Fold Cross-Validation** for **robust evaluation**.  

---

## 📜 License  
This project involves dataset integration and processing for Parkinson’s disease severity prediction. It incorporates datasets with specific usage restrictions.  

### 📄 License Details  
- **[Mendeley Gait Data](https://doi.org/10.17632/4tjd8jrhp8.1)** is licensed under **[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)**.
- **[Kaggle AMP®-Parkinson's Dataset](https://www.kaggle.com/competitions/amp-parkinsons-disease-progression-prediction/data)** is **restricted to non-commercial & academic research use only** as per Kaggle’s competition terms. To access the data, please visit **[Kaggle](https://www.kaggle.com/competitions/amp-parkinsons-disease-progression-prediction/data)**.  
- **This repository is licensed under** **[Creative Commons Attribution-NonCommercial 4.0 (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/)**.  

📌 **This means you can share, modify, and use the work for research purposes, but commercial use is strictly prohibited.**  

📄 **See the [LICENSE](LICENSE) file for full details.**  
 

---

## **🙏 Acknowledgments**  
We extend our gratitude to the organizations and researchers who provided **raw datasets** that made this study possible:  

- **[AMP Parkinson’s Disease Progression Prediction Data (Kaggle)](https://www.kaggle.com/competitions/amp-parkinsons-disease-progression-prediction/data)**
- **[Gait Data Repository (Mendeley)](https://doi.org/10.17632/4tjd8jrhp8.1)**  

Additionally, we acknowledge:  
- **[MDS-UPDRS](https://www.movementdisorders.org/MDS/MDS-Rating-Scales/MDS-Unified-Parkinsons-Disease-Rating-Scale-MDS-UPDRS.htm)** clinical framework for Parkinson’s disease assessment.  

---

  
