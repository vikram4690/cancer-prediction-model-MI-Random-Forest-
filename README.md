# 🧬 Cancer Type Prediction from Gene Expression  

This project uses **machine learning** to predict the type of cancer based on **gene expression profiles**.  
A **Random Forest classifier** (with One-vs-Rest strategy) is trained to classify 5 cancer types.  
A **Gradio web interface** is included so you can test predictions interactively.  

---

## 📌 Dataset  

- **Source**: [Cancer Gene Expression Dataset](https://github.com/vappiah/Machine-Learning-Tutorials/raw/main/datasets/cancer_gene_expression.zip)  
- **Shape**: `801 samples × 20,532 columns`  
- **Classes (Cancer Types)**:  
  - **BRCA** → Breast Invasive Carcinoma  
  - **KIRC** → Kidney Renal Clear Cell Carcinoma  
  - **LUAD** → Lung Adenocarcinoma  
  - **PRAD** → Prostate Adenocarcinoma  
  - **COAD** → Colon Adenocarcinoma  

---

## ⚙️ Workflow  

1. **Data Preprocessing**  
   - Missing value check  
   - Label encoding for cancer types  
   - Min-Max normalization of features  
   - Feature selection using **Mutual Information (Top 300 features)**  

2. **Model Training**  
   - Random Forest Classifier (One-vs-Rest)  
   - Evaluation with Accuracy, Precision, Recall, F1-score  

3. **Evaluation Metrics**  
   - Balanced Accuracy  
   - Weighted Precision, Recall, F1-score  
   - Confusion Matrix & ROC Curves  

4. **Model Saving**  
   - `rf_model.pkl` → Trained model  
   - `scaler.pkl` → MinMaxScaler  
   - `label_encoder.pkl` → Label encoder  
   - `selected_features.pkl` → Top 300 features  

5. **Gradio Web App**  
   - Paste in a **gene expression sequence** (20531 values, comma-separated)  
   - Get a predicted **cancer type** instantly  

---

## 🚀 Usage  

### 1. Clone Repository  
```bash
git clone https://github.com/your-username/cancer-prediction.git
cd cancer-prediction
