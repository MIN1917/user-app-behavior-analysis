# 📱 User Mobile App Behavior Analysis

本專案使用 Kaggle [User Mobile App Interaction Data](https://www.kaggle.com/datasets/xxx)  
目標是找出影響轉換的關鍵互動行為（key interaction behaviors leading to conversion）。

---

## 📂 專案結構
user-app-behavior-analysis/
│── data/
│ ├── user_mobile_app_interaction_data.csv # 原始 Kaggle 資料（需自行下載，已 .gitignore）
│ └── processed_app_interactions.csv # 清理後的資料（已附）
│── notebooks/
│ ├── 00_cleaning.ipynb # 資料清理流程（型別轉換、缺失值處理、異常值處理）
│ ├── 01_EDA.ipynb # 探索性資料分析 (EDA)
│── scripts/ # 預留 ETL / feature 工具程式
│── reports/ # 圖表與分析文件
│── requirements.txt
│── README.md

---

## 🚀 使用方式
### 1. 下載資料
1. 到 Kaggle 下載原始資料集：[User Mobile App Interaction Data](https://www.kaggle.com/datasets/mohamedmoslemani/user-mobile-app-interaction-data)  
2. 放到 `data/` 資料夾下，命名為 `user_mobile_app_interaction_data.csv`

### 2. 建立虛擬環境並安裝套件
```bash
python -m venv venv
venv\Scripts\activate   # Windows
# source venv/bin/activate   # Mac/Linux

pip install -r requirements.txt

### 3. 跑資料清理
jupyter lab notebooks/00_cleaning.ipynb
會輸出 data/processed_app_interactions.csv

### 4. 跑 EDA 分析
jupyter lab notebooks/01_EDA.ipynb

📝 備註

data/user_mobile_app_interaction_data.csv 不會上傳到 GitHub（已 .gitignore），需自行下載

data/processed_app_interactions.csv 已包含在 repo 中，可直接使用

專案後續會擴展至 feature engineering / modeling / dashboard