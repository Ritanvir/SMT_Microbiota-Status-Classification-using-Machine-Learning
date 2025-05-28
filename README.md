# SMT_Microbiota-Status-Classification-using-Machine-Learning
Project Overview: Gut Microbiota Classification
This project aims to build a machine learning model, specifically a transformer-based architecture, to classify an individual's gut microbiota status into one of the following categories:

1. Optimal

2. Suboptimal

3. At Risk

The classification is based on multiple factors:

Health indicators (e.g., BMI, diagnosed conditions)

Lifestyle habits (e.g., smoking, exercise, sleep)

Diet and gastrointestinal symptoms

The goal is not only accurate prediction but also interpretability using SHAP values and advanced models like TabTransformer.

📊 Dataset Description
The dataset (health_data_10000_chunk.xlsx) includes 10,000+ patient records, each with the following features:

🔹 Key Feature Categories:
Demographics: Height, Weight, BMI

Medical History: Diagnosed conditions, family disease history, surgeries

Lifestyle: Physical activity, sleep, smoking, stress

Diet: Weekly intake of vegetables, fruits, proteins, fermented foods, water, alcohol

Gastrointestinal Health: Bowel frequency, stool consistency, bloating, gas, pain

🎯 Target Variable:
Current status of microbiota: {Optimal, Suboptimal, At Risk}

⚙️ Setup Instructions (Google Colab Compatible)
🔧 1. Install Required Libraries:

!pip install -q pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn shap openpyxl
!pip install -q torch==2.0.1 torchvision==0.15.2 torchaudio==2.0.2 --index-url https://download.pytorch.org/whl/cpu
!pip install -q pytorch-lightning==2.0.8
!pip install -q pytorch-tabular==1.1.0

📁 2. Upload Data File:
Upload health_data_10000_chunk.xlsx to your Colab environment.

✅ Key Results
🔹 Baseline Model (Random Forest):
Performed well on initial evaluation.

Used SMOTE to address class imbalance.

SHAP explained top influential features:

BMI, Fruit intake, Fermented foods, Stress level, Stool consistency

🔹 TabTransformer Model:
Outperformed traditional models on multiclass accuracy and F1-score.

Automatically handled both categorical and continuous data.

Great candidate for medical tabular data applications.

📊 Example Metrics:
Accuracy: ~82%

F1-Score: ~0.80 (varied across classes)

AUC-ROC: Visualized per class (macro/micro average)

