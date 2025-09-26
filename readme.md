# 🏦 Semi Supervised Learning (Pseudo Labeling) on Bank Transactions using Clustering & Classification  

## 📌 Overview  
This project explores **pseudo-labeling** as a semi-supervised learning strategy, applied to a **bank transactions dataset**.  

The workflow combines **clustering** and **classification** to assign pseudo-labels to unlabeled data and improve supervised training performance. By leveraging both raw and PCA-reduced feature spaces, the project aims to enhance classification accuracy and model generalization.  

---

## 📊 Dataset  
The dataset consists of **bank transaction records**, containing both numerical and categorical features. Example columns include:  

- `TransactionAmount` 💵  
- `TransactionDate` 🗓️  
- `TransactionType`  
- `Location`  
- `Channel`  
- `CustomerAge` 👤  
- `CustomerOccupation`  
- `TransactionDuration` ⏳  
- `LoginAttempts` 🔑  
- `AccountBalance`  
- `PreviousTransactionDate`  

Additionally, engineered features such as `AgeGroup_encoded`, `AmountGroup_encoded`, and **Target labels** (from clustering pseudo-labels) were included.  

---

## ⚙️ Methodology  

### 🔹 1. Data Preprocessing  
- Handling missing values  
- Normalization of continuous features  
- Encoding categorical variables  
- Feature engineering from temporal and amount-based fields  

### 🔹 2. Clustering (Pseudo-Labeling)  
Two approaches were tested:  
- **Clustering on raw normalized features**  
- **Clustering on PCA-reduced features**  

Clustering algorithms help generate **pseudo-labels** for initially unlabeled data.  

### 🔹 3. Classification Models  
Pseudo-labeled data was then used to train classification models:  
- 🌳 **Decision Tree**  
- 🌲 **Random Forest**  
- 🤖 **Multi-Layer Perceptron (MLP)**  

### 🔹 4. Hyperparameter Tuning  
Models were fine-tuned using grid/random search to optimize:  
- Depth, number of estimators (Tree-based)  
- Learning rate, hidden layers (MLP)  

---

## 🚀 Experiments & Results  
- **Clustering with PCA** showed better separation of transaction patterns compared to raw features.  
- **Random Forest** achieved the best trade-off between accuracy and generalization.  
- **MLP** improved with tuned hidden layers but required careful regularization to avoid overfitting.  
- **Pseudo-labeling** enhanced classification performance compared to using only original labeled data.  

---

## 📈 Key Insights  
- Pseudo-labeling can effectively leverage unlabeled transaction data.  
- Dimensionality reduction (PCA) can significantly improve cluster quality.  
- Ensemble methods (Random Forest) remain strong baselines for structured financial data.  

---

## 🛠️ Tech Stack  
- **Python** 🐍  
- Libraries: `scikit-learn`, `numpy`, `pandas`, `matplotlib`, `seaborn`  

---

## 📂 Project Structure  
    ├── data/ # Raw and processed datasets
    ├── src/ # EDA - Preprocessing - Model Experiment notebooks  
    ├── model_results/ # Saved Models
    └── README.md # Project documentation


## 🔮 Future Work  
- Experiment with advanced clustering (DBSCAN, HDBSCAN)  
- Apply semi-supervised learning techniques beyond pseudo-labeling  
- Evaluate deep learning methods (TabNet, Autoencoders)  
- Incorporate explainability (SHAP, LIME) for financial insights  

---

## 👤 Author  
**Jeremy Mattathias Mboe**  
📚 AI Student at Institut Teknologi Sepuluh Nopember| 🤖 ML & DL Enthusiast | 

