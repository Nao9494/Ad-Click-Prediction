# 廣告點擊預測分析｜數據分析｜XGBoost97%

本項目旨在利用機器學習技術預測用戶是否會點擊廣告。通過探索性數據分析 (EDA) 和模型訓練，這個項目展示了如何從數據集中提取信息並進行預測建模。

### 目錄

1. [介紹](#介紹)
2. [數據集](#數據集)
3. [技術工具](#技術工具)
4. [分析過程](#分析過程)
5. [模型調參](#模型調參)
6. [結果與結論](#結果與結論)
7. [如何運行項目](#如何運行項目)

---

## 介紹
透過分析用戶行為數據，構建一個預測模型，判斷用戶是否會點擊廣告。這個分析包括對數據的清理、探索性數據分析、特徵工程以及機器學習模型的訓練與參數調優。

## 數據集

數據集包含廣告用戶的點擊行為，主要字段包括：
- **user_id**: 用戶唯一標識
- **age**: 用戶年齡
- **gender**: 用戶性別
- **device**: 使用的設備類型（桌面、手機等）
- **ad_position**: 廣告顯示位置（頂部、側邊等）
- **ad_category**: 廣告類別（購物、教育等）
- **time_of_day**: 廣告顯示的時間（上午、下午、晚上等）
- **click**: 是否點擊廣告的標籤（1 表示點擊，0 表示未點擊）

數據集經過了清理處理，去除了缺失值和不必要的字段。

> **本專案使用的資料集來源於 Kaggle**: https://www.kaggle.com/datasets/marius2303/ad-click-prediction-dataset

## 技術工具

在本項目中，我們使用了以下技術工具：
- **Python 3.12**
- **Pandas**：數據處理
- **NumPy**：數據操作
- **Matplotlib / Seaborn / Plotly Express**：數據可視化
- **Scikit-learn**：模型訓練與評估
- **XGBoost**：梯度提升決策樹
- **ADASYN**：處理不平衡數據的過採樣技術

## 分析過程

1. **數據清理**：處理缺失值，去除無意義的列（如`user_id`）。
2. **探索性數據分析 (EDA)**：
   - 使用數據可視化工具查看數據分佈
   - 分析點擊行為與年齡、性別、設備等變量的關係
3. **特徵工程**：
   - 處理類別型變量
   - 使用 KNNImputer 填補缺失的年齡值，並將類別變量映射回原始類別
4. **模型構建與評估**：
   - 使用 `XGBoost` 構建模型
   - 使用混淆矩陣、分類報告評估模型性能

## 模型調參

在模型訓練中，我們使用了 `GridSearchCV` 對 XGBoost 模型進行調參。主要調參範圍包括：
- `learning_rate`：學習率
- `n_estimators`：決策樹數量
- `max_depth`：樹的最大深度

通過五折交叉驗證，我們找到的最佳參數如下：
Best Parameters: { 'learning_rate': 0.2, 'n_estimators': 200, 'max_depth': 7 }
## 結果與結論

模型的最佳性能通過分類報告和混淆矩陣來評估，最終模型的準確率為 **97%**。根據模型的預測結果，可以有效區分點擊和未點擊的用戶群體。

## 如何運行項目
1. 複製倉庫到本地：
- git clone https://github.com/Nao9494/Ad_Click_Prediction.git
2. 快速安裝所需的資料庫：
- pip install -r requirements.txt 
3. 運行 Jupyter Notebook 進行數據分析：
- jupyter notebook Ad_Click_Prediction.ipynb

---
# README.md
- en [English](README.md)
- zh_TW [繁体中文](README.zh_TW.md)
