# 🏏 Cricket Match Win Prediction

## 🎯 Objective
Predict the **winning team** of a cricket match *before it begins* using pre-match features such as teams, toss result, toss decision, venue, and season.

## ⚙️ Project Pipeline
1. Data collection & cleaning  
2. Exploratory Data Analysis (EDA)  
3. Feature engineering  
4. Time-aware train/test split  
5. Model training (Logistic Regression, Random Forest)  
6. Evaluation (Accuracy, Confusion Matrix, SHAP)  
7. Save model & make predictions

## 📁 Project Structure

data/            # Raw and processed data  
src/             # Scripts (preprocess, train, predict)  
out/             # Trained model  
requirements.txt  
README.md  


## 🚀 How to Run
### 1. Install dependencies
```bash
pip install -r requirements.txt
````

### 2. Preprocess the data

```bash
python src/preprocess.py --input data/matches.csv --output data/processed.csv
```

### 3. Train the model

```bash
python src/train.py --data data/processed.csv --model out/model.pkl
```

### 4. Predict match outcome

```bash
python src/predict.py --model out/model.pkl --match "TeamA,TeamB,venue,toss_winner,toss_decision,season"
```

Example:

```bash
python src/predict.py --model out/model.pkl --match "CSK,MI,Chennai,CSK,bat,2023"
```

Output:

```
Predicted Winner: CSK
```

---

## 🧠 Tech Stack

* Python
* pandas, scikit-learn, shap, joblib
* Logistic Regression & Random Forest

---

## 👨‍💻 Author

**Priyanshu Mallick**
[GitHub Profile](https://github.com/PriyanshuM04)