# 📊 Evaluating Learning Rate Effects on Long Short-Term Memory for Indonesian Sentiment Classification

## 📄 Research Paper

**Authors:**  
Serly Eldina, Tekad Matulatan, Novrizal Fattah Fahmitra  

**Affiliation:**  
Universitas Maritim Raja Ali Haji, Indonesia  

**Year:**  
2025  

**🔗 Link to Paper:**  
[📘 View Full Paper](https-)

---
## 🧠 Architecture
![Alt Text](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/architecture.png)
---

## 📁 Dataset  

- **Type:** Indonesian Sentiment Text Data  
- **Domains:**  
  - **In-domain:** App Reviews (*Sirekap* – Google Play Store)  
  - **Cross-domain:** News Headlines (*Topic: Makanan Bergizi Gratis / MBG*)  
- **Format:** `.xlsx` (Microsoft Excel)

---

### 📦 Available Datasets  

| Dataset Type | Description | Download Link |
|---------------|-------------|----------------|
| **Full Dataset (In-domain)** | Complete dataset of *App Reviews Sirekap* before train/test splitting. | [⬇️ Download Full In-domain Dataset (Excel)](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Dataset/datalabel.csv) |
|**Full Dataset (In-domain)** | Complete dataset of *App Reviews Sirekap* before train/test splitting. data undersampling | [⬇️ Download Full In-domain Dataset Undersampling (Excel)](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Dataset/data_undersampling.csv) |
| **Test Dataset (In-domain)** | Test set obtained from splitting the *App Reviews Sirekap* dataset. | [⬇️ Download In-domain Test Dataset (Excel)](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/raw/main/Dataset/Dataset_Test_InDomain.xlsx) |
| **Test Dataset (Cross-domain)** | Test set from the *News Headlines* domain with the topic *Makanan Bergizi Gratis (MBG)*. | [⬇️ Download Cross-domain Test Dataset (Excel)](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Dataset/test_set_in_domain_sirekap.csv) |

---

> 💡 *Click the links above to directly download the Excel dataset. If it does not download automatically, right-click → “Save link as…” to save the file.*

## ⚙️ Experimental Settings

| **Hyperparameter**   | **Value**                               |
| -------------------- | --------------------------------------- |
| Model                | LSTM                                    |
| Optimizer            | Adam                                    |
| Epochs               | 50 *(Early Stopping applied)*           |
| Batch Size           | 32                                      |
| Learning Rate Tested | 0.0001, 0.001, 0.002, 0.005, 0.01, 0.02 |
| Embedding Dimension  | 64                                      |
| LSTM Units           | 32                                      |
| Dense Units          | 3                                       |
| Dropout              | 0.2                                     |
| Metric               | Confusion Matrix                               |

---

## TRAINING MODEL 10 FOLD LR (0.0001, 0.001, 0.002, 0.01, 0,02)

## 🧠 Training Model 10-Fold (LSTM)
### Learning Rate Variation Results (0.0001 – 0.02)

---

### 📊 Overall 10-Fold Comparison
<img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/10-Fold%20Cross%20Validation%20Learning%20Rate%20Comparison.png" width="90%">

---

<details>
  <summary><b>🔹 LR = 0.0001</b></summary>

  <br>

  | Fold | Learning Rate | Train Accuracy | Train Loss | Validation Accuracy | Validation Loss |
  |:----:|:--------------:|:---------------:|:------------:|:-------------------:|:----------------:|
  | 1 | 0.0001 | 0.9045 | 0.3182 | 0.8100 | 0.5407 |
  | 2 | 0.0001 | 0.8936 | 0.3430 | 0.8172 | 0.5100 |
  | 3 | 0.0001 | 0.9041 | 0.3276 | 0.8065 | 0.5656 |
  | 4 | 0.0001 | 0.9114 | 0.2942 | 0.8268 | 0.5326 |
  | 5 | 0.0001 | 0.8973 | 0.3289 | 0.8029 | 0.5374 |
  | 6 | 0.0001 | 0.9107 | 0.2883 | 0.8002 | 0.5748 |
  | 7 | 0.0001 | 0.9024 | 0.3272 | 0.7895 | 0.5351 |
  | 8 | 0.0001 | 0.8971 | 0.3297 | 0.8098 | 0.5175 |
  | 9 | 0.0001 | 0.8818 | 0.3826 | 0.7895 | 0.5749 |
  | 10 | 0.0001 | 0.8819 | 0.3814 | 0.7883 | 0.5670 |

### 📈 Training Results per Epoch (Each Fold)

The following file contains detailed training results for each epoch across all 10 folds at a learning rate of **0.0001**. You can view the accuracy and loss progression for every fold in the Excel sheet below:

  <div align="left">
    <a href="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/experiment-results/trainingLR0.0001_10FOLD.xlsx">
      <img src="https://img.shields.io/badge/View%20Excel%20(0.0001)-blue?style=for-the-badge&logo=microsoft-excel&logoColor=white">
    </a>
  </div>

</details>

---

<details>
 <summary><b>🔹 LR = 0.001</b></summary>

  <br>

  | Fold | Learning Rate | Train Accuracy | Train Loss | Validation Accuracy | Validation Loss |
  |:----:|:--------------:|:---------------:|:------------:|:-------------------:|:----------------:|
  | 1 | 0.001 | 0.8462 | 0.4433 | 0.7993 | 0.5383 |
  | 2 | 0.001 | 0.8383 | 0.4431 | 0.8280 | 0.4790 |
  | 3 | 0.001 | 0.8806 | 0.3329 | 0.8148 | 0.5093 |
  | 4 | 0.001 | 0.8440 | 0.4530 | 0.8065 | 0.5200 |
  | 5 | 0.001 | 0.8375 | 0.4543 | 0.8088 | 0.5086 |
  | 6 | 0.001 | 0.8415 | 0.4588 | 0.8050 | 0.5116 |
  | 7 | 0.001 | 0.8422 | 0.4508 | 0.7895 | 0.5182 |
  | 8 | 0.001 | 0.8348 | 0.4559 | 0.8074 | 0.4962 |
  | 9 | 0.001 | 0.8463 | 0.4407 | 0.7907 | 0.5185 |
  | 10 | 0.001 | 0.8342 | 0.4569 | 0.7919 | 0.5037 |

### 📈 Training Results per Epoch (Each Fold)

The following file contains detailed training results for each epoch across all 10 folds at a learning rate of **0.001**. You can view the accuracy and loss progression for every fold in the Excel sheet below:

  <div align="left">
    <a href="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/experiment-results/trainingLR0.001_10FOLD.xlsx" target="_blank">
      <img src="https://img.shields.io/badge/View%20Excel%20(0.001)-success?style=for-the-badge&logo=microsoft-excel&logoColor=white">
    </a>
  </div>

</details>

---

<details>
  <summary><b>🔹 LR = 0.002 </b></summary>

  <br>

  (tabel 10 fold 0.002 di sini...)
  
### 📈 Training Results per Epoch (Each Fold)

The following file contains detailed training results for each epoch across all 10 folds at a learning rate of **0.002**. You can view the accuracy and loss progression for every fold in the Excel sheet below:

  <div align="left">
    <a href="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/experiment-results/trainingLR0.002_10FOLD.xlsx" target="_blank">
      <img src="https://img.shields.io/badge/View%20Excel%20(0.002)-brightgreen?style=for-the-badge&logo=microsoft-excel&logoColor=white">
    </a>
  </div>

</details>

---

<details>
  <summary><b>🔹 LR = 0.005 — Moderate</b></summary>

  <br>

  (tabel 10 fold 0.005 di sini...)

### 📈 Training Results per Epoch (Each Fold)

The following file contains detailed training results for each epoch across all 10 folds at a learning rate of **0.005**. You can view the accuracy and loss progression for every fold in the Excel sheet below:

  <div align="left">
    <a href="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/experiment-results/trainingLR0.005_10FOLD.xlsx" target="_blank">
      <img src="https://img.shields.io/badge/View%20Excel%20(0.005)-orange?style=for-the-badge&logo=microsoft-excel&logoColor=white">
    </a>
  </div>

</details>

---

<details>
  <summary><b>🔹 LR = 0.01 — Slightly Unstable</b></summary>

  <br>

  (tabel 10 fold 0.01 di sini...)

  <div align="left">
    <a href="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/experiment-results/trainingLR0.01_10FOLD.xlsx" target="_blank">
      <img src="https://img.shields.io/badge/View%20Excel%20(0.01)-red?style=for-the-badge&logo=microsoft-excel&logoColor=white">
    </a>
  </div>

</details>

---

<details>
  <summary><b>🔹 LR = 0.02 — Lowest</b></summary>

  <br>

  (tabel 10 fold 0.02 di sini...)

  <div align="left">
    <a href="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/experiment-results/trainingLR0.02_10FOLD.xlsx" target="_blank">
      <img src="https://img.shields.io/badge/View%20Excel%20(0.02)-gray?style=for-the-badge&logo=microsoft-excel&logoColor=white">
    </a>
  </div>

</details>


---
<details>
  <summary><h2>📊 Statistical Analysis (Click to expand full results)</h2></summary>

<br>

### 🔹 One-Way ANOVA Test

| Source | DF | Sum Sq | Mean Sq | F-value | P-value | Significance |
|--------|----|--------|---------|----------|----------|---------------|
| Learning Rate | 5 | 0.004658 | 0.000932 | 5.1989 | 0.000575 | ✅ Significant |
| Residual | 54 | 0.009676 | 0.000179 | — | — | — |

---

### 🔹 Assumption Testing

| Test | Statistic | P-value | Result | Interpretation |
|------|------------|----------|----------|----------------|
| Shapiro–Wilk (Normality) | 0.9614 | 0.0553 | ✅ Pass | Data are normally distributed |
| Levene’s Test (Homogeneity) | 1.3639 | 0.2524 | ✅ Pass | Variances are homogeneous |


---

### 🔹 Descriptive Statistics 

| Learning Rate | N | Mean | Std Dev | Min | Max | 
|---------------|---|------|----------|-----|-----|
| ACC_0.0001 | 10 | 0.8041 | 0.0127 | 0.7883 | 0.8268 | 
| ACC_0.001 | 10 | 0.8042 | 0.0120 | 0.7895 | 0.8280 | 
| ACC_0.002 | 10 | 0.7974 | 0.0133 | 0.7811 | 0.8208 | 
| ACC_0.005 | 10 | 0.7962 | 0.0105 | 0.7787 | 0.8076 | 
| ACC_0.01 | 10 | 0.7874 | 0.0208 | 0.7656 | 0.8232 | 
| ACC_0.02 | 10 | 0.7797 | 0.0072 | 0.7703 | 0.7921 | 


---

### 🔹 Post-hoc Tukey HSD 

| Group 1 | Group 2 | Mean Diff | P-adj | Lower | Upper | Significant |
|----------|----------|-----------|--------|--------|--------|--------------|
| ACC_0.0001 | ACC_0.001 | 0.0001 | 1.0000 | -0.0176 | 0.0178 | ❌ No |
| ACC_0.0001 | ACC_0.002 | -0.0067 | 0.8706 | -0.0244 | 0.0110 | ❌ No |
| ACC_0.0001 | ACC_0.005 | -0.0079 | 0.7739 | -0.0256 | 0.0098 | ❌ No |
| ACC_0.0001 | ACC_0.01 | -0.0166 | 0.0764 | -0.0343 | 0.0010 | ❌ No |
| ACC_0.0001 | ACC_0.02 | -0.0244 | 0.0020 | -0.0421 | -0.0067 | ✅ Yes |
| ACC_0.001 | ACC_0.002 | -0.0068 | 0.8620 | -0.0245 | 0.0109 | ❌ No |
| ACC_0.001 | ACC_0.005 | -0.0080 | 0.7627 | -0.0257 | 0.0097 | ❌ No |
| ACC_0.001 | ACC_0.01 | -0.0168 | 0.0729 | -0.0344 | 0.0009 | ❌ No |
| ACC_0.001 | ACC_0.02 | -0.0245 | 0.0019 | -0.0422 | -0.0068 | ✅ Yes |
| ACC_0.002 | ACC_0.005 | -0.0012 | 1.0000 | -0.0189 | 0.0165 | ❌ No |
| ACC_0.002 | ACC_0.01 | -0.0099 | 0.5643 | -0.0276 | 0.0078 | ❌ No |
| ACC_0.002 | ACC_0.02 | -0.0177 | 0.0499 | -0.0354 | 0.0000 | ✅ Yes |
| ACC_0.005 | ACC_0.01 | -0.0087 | 0.6895 | -0.0264 | 0.0089 | ❌ No |
| ACC_0.005 | ACC_0.02 | -0.0165 | 0.0804 | -0.0342 | 0.0012 | ❌ No |
| ACC_0.01 | ACC_0.02 | -0.0078 | 0.7858 | -0.0254 | 0.0099 | ❌ No |

---

### 🔹 Effect Size

| Metric | Value | Interpretation |
|---------|--------|----------------|
| Eta Squared (η²) | 0.3250 | Large Effect |

---

### 🧾 Overall Summary

| Metric | Result |
|---------|---------|
| ANOVA P-value | 0.000575 |
| Effect Size (η²) | 0.3250 |
| Significant? | ✅ Yes |
| Significant Differences | 0.0001 vs 0.02, 0.001 vs 0.02, 0.002 vs 0.02 |

---


</details>


## 🧮 Visualization

---

## 📉 Training Curves per Learning Rate

Klik setiap *learning rate* untuk melihat 10 kurva pelatihannya.  
(Gambar diambil dari folder `/curve/`)

---

<details>
  <summary>🔹 <b>Learning Rate = 0.0001</b></summary>

  ![LR 0.0001 fold 1](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold1_lr0.0001.png)
  ![LR 0.0001 fold 2](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold2_lr0.0001.png)
  ![LR 0.0001 fold 3](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold3_lr0.0001.png)
  ![LR 0.0001 fold 4](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold4_lr0.0001.png)
  ![LR 0.0001 fold 5](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold5_lr0.0001.png)
  ![LR 0.0001 fold 6](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold6_lr0.0001.png)
  ![LR 0.0001 fold 7](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold7_lr0.0001.png)
  ![LR 0.0001 fold 8](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold8_lr0.0001.png)
  ![LR 0.0001 fold 9](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold9_lr0.0001.png)
  ![LR 0.0001 fold 10](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold10_lr0.0001.png)
</details>

---

<details>
  <summary>🔹 <b>Learning Rate = 0.001</b></summary>

  ![LR 0.001 fold 1](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold1_lr0.001.png)
  ![LR 0.001 fold 2](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold2_lr0.001.png)
  ![LR 0.001 fold 3](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold3_lr0.001.png)
  ![LR 0.001 fold 4](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold4_lr0.001.png)
  ![LR 0.001 fold 5](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold5_lr0.001.png)
  ![LR 0.001 fold 6](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold6_lr0.001.png)
  ![LR 0.001 fold 7](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold7_lr0.001.png)
  ![LR 0.001 fold 8](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold8_lr0.001.png)
  ![LR 0.001 fold 9](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold9_lr0.001.png)
  ![LR 0.001 fold 10](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold10_lr0.001.png)
</details>

---

<details>
  <summary>🔹 <b>Learning Rate = 0.002</b></summary>

  ![LR 0.002 fold 1](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold1_lr0.002.png)
  ![LR 0.002 fold 2](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold2_lr0.002.png)
  ![LR 0.002 fold 3](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold3_lr0.002.png)
  ![LR 0.002 fold 4](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold4_lr0.002.png)
  ![LR 0.002 fold 5](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold5_lr0.002.png)
  ![LR 0.002 fold 6](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold6_lr0.002.png)
  ![LR 0.002 fold 7](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold7_lr0.002.png)
  ![LR 0.002 fold 8](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold8_lr0.002.png)
  ![LR 0.002 fold 9](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold9_lr0.002.png)
  ![LR 0.002 fold 10](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold10_lr0.002.png)
</details>

---

<details>
  <summary>🔹 <b>Learning Rate = 0.005</b></summary>

  ![LR 0.005 fold 1](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold1_lr0.005.png)
  ![LR 0.005 fold 2](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold2_lr0.005.png)
  ![LR 0.005 fold 3](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold3_lr0.005.png)
  ![LR 0.005 fold 4](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold4_lr0.005.png)
  ![LR 0.005 fold 5](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold5_lr0.005.png)
  ![LR 0.005 fold 6](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold6_lr0.005.png)
  ![LR 0.005 fold 7](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold7_lr0.005.png)
  ![LR 0.005 fold 8](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold8_lr0.005.png)
  ![LR 0.005 fold 9](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold9_lr0.005.png)
  ![LR 0.005 fold 10](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold10_lr0.005.png)
</details>

---

<details>
  <summary>🔹 <b>Learning Rate = 0.01</b></summary>

  ![LR 0.01 fold 1](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold1_lr0.01.png)
  ![LR 0.01 fold 2](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold2_lr0.01.png)
  ![LR 0.01 fold 3](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold3_lr0.01.png)
  ![LR 0.01 fold 4](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold4_lr0.01.png)
  ![LR 0.01 fold 5](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold5_lr0.01.png)
  ![LR 0.01 fold 6](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold6_lr0.01.png)
  ![LR 0.01 fold 7](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold7_lr0.01.png)
  ![LR 0.01 fold 8](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold8_lr0.01.png)
  ![LR 0.01 fold 9](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold9_lr0.01.png)
  ![LR 0.01 fold 10](https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Salinan%20training_curves_fold10_lr0.01.png)
</details>

---

<details>
  <summary>🔹 <b>Learning Rate = 0.02</b></summary>

  ![LR 0.02 fold 1](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/blob/main/build/Salinan%20training_curves_fold1_lr0.02.png)
  ![LR 0.02 fold 2](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/blob/main/build/Salinan%20training_curves_fold2_lr0.02.png)
  ![LR 0.02 fold 3](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/blob/main/build/Salinan%20training_curves_fold3_lr0.02.png)
  ![LR 0.02 fold 4](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/blob/main/build/Salinan%20training_curves_fold4_lr0.02.png)
  ![LR 0.02 fold 5](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/blob/main/build/Salinan%20training_curves_fold5_lr0.02.png)
  ![LR 0.02 fold 6](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/blob/main/build/Salinan%20training_curves_fold6_lr0.02.png)
  ![LR 0.02 fold 7](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/blob/main/build/Salinan%20training_curves_fold7_lr0.02.png)
  ![LR 0.02 fold 8](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/blob/main/build/Salinan%20training_curves_fold8_lr0.02.png)
  ![LR 0.02 fold 9](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/blob/main/build/Salinan%20training_curves_fold9_lr0.02.png)
  ![LR 0.02 fold 10](https://github.com/Serly-Eldina/LSTM-learning-rate-research-data-/blob/main/build/Salinan%20training_curves_fold10_lr0.02.png)
</details>


---
---

## 🔍 Confusion Matrix Results

Klik untuk melihat confusion matrix hasil pengujian model pada data **in-domain** dan **cross-domain**.

---

### 🔹 Confusion Matrix Results (In-Domain)

<table align="center">
  <tr>
    <td align="center">
      <h4>LR = 0.0001</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold4LR0.0001indomain.png?raw=true" width="95%">
    </td>
    <td align="center">
      <h4>LR = 0.001</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold2LR0.001indomain.png?raw=true" width="95%">
    </td>
    <td align="center">
      <h4>LR = 0.002</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold2LR0.002indomain.png?raw=true" width="95%">
    </td>
  </tr>
  <tr>
    <td align="center">
      <h4>LR = 0.005</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold1LR0.005indomain.png?raw=true" width="95%">
    </td>
    <td align="center">
      <h4>LR = 0.01</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold5LR0.01indomain.png?raw=true" width="95%">
    </td>
    <td align="center">
      <h4>LR = 0.02</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold2LR0.02indomain.png?raw=true" width="95%">
    </td>
  </tr>
</table>

### 🔹 Confusion Matrix Results (Cross-Domain)

<table align="center">
  <tr>
    <td align="center">
      <h4>LR = 0.0001</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold4LR0.0001crossdomain.png?raw=true" width="95%">
    </td>
    <td align="center">
      <h4>LR = 0.001</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold2LR0.001crossdomain.png?raw=true" width="95%">
    </td>
    <td align="center">
      <h4>LR = 0.002</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold2LR0.002crossdomain.png?raw=true" width="95%">
    </td>
  </tr>
  <tr>
    <td align="center">
      <h4>LR = 0.005</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold1LR0.005crossdomain.png?raw=true" width="95%">
    </td>
    <td align="center">
      <h4>LR = 0.01</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold5LR0.01crossdomain.png?raw=true" width="95%">
    </td>
    <td align="center">
      <h4>LR = 0.02</h4>
      <img src="https://github.com/Serly-Eldina/LSTM-LearningRate-Indonesia-Sentiment/blob/main/Images/Confusionmatrixfold2LR0.02crossdomain.png?raw=true" width="95%">
    </td>
  </tr>
</table>




---

© 2025 Serly Eldina, Tekad Matulatan, Novrizal Fattah Fahmitra 2025 
