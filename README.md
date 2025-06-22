# AI-in-liver-cirrhosis-A-model-for-stage-classification

This project presents an explainable AI-based framework for non-invasive diagnosis and staging of liver cirrhosis, focusing specifically on Primary Biliary Cirrhosis (PBC) using serum biomarkers. Unlike conventional methods that rely on imaging techniques or invasive biopsies, this approach offers a transparent, interpretable, and accurate machine learning pipeline for clinical decision support.

🩺 Motivation

Liver cirrhosis is a chronic and progressive condition triggered by prolonged liver damage due to factors such as:
- Alcohol consumption
- Hepatotoxic drug exposure
- Non-alcoholic steatohepatitis (NASH)

Given the risks and costs of liver biopsy, there is a growing need for non-invasive diagnostic tools. Existing methods often use imaging modalities (MRI, ultrasound, elastography) paired with machine learning—but serum biomarkers remain underutilized despite being clinically valuable and cost-effective.

🔍 Key Contributions

- ✅ Uses serum biomarkers for liver cirrhosis staging
- ✅ Employs Hidden Markov Models (HMMs) to uncover latent progression patterns
- ✅ Applies XGBoost classifier fine-tuned via Optuna
- ✅ Enhances trust through Explainable AI (XAI) for model transparency
- ✅ Implements custom threshold optimization to fine-tune classification outputs
- ✅ Achieves 88% overall accuracy
  - AUC Scores:
    - Class 0: 1.00
    - Classes 1 & 3: 0.96
    - Class 2: 0.88
          
🧠 Technologies & Libraries

- Python
- XGBoost
- Hidden Markov Models (HMMlearn / custom)
- Optuna (hyperparameter tuning)
- SHAP / LIME (for explainability)
- Scikit-learn
- NumPy, Pandas, Matplotlib, Seaborn
  
⚙️ How the Pipeline Works

1. Data Preprocessing
   - Clean and normalize serum biomarker data
   - Encode target labels for staging

2. Latent Stage Modeling
   - Use HMM to detect hidden progression patterns from biomarker sequences

3. Classification
   - Feed HMM outputs and biomarker features into a **tuned XGBoost classifier**

4. Threshold Optimization
   - Customize thresholds to improve sensitivity-specificity tradeoff

5. Explainability
   - Generate SHAP/LIME plots to interpret model predictions

📈 Results

| Metric          | Value        |
|-----------------|--------------|
| Accuracy        | 88%          |
| AUC (Class 0)   | 1.00         |
| AUC (Class 1/3) | 0.96         |
| AUC (Class 2)   | 0.88         |


