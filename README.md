# Insurance Fraud Detection using Decision Tree & Random Forest

---

##  Project Structure

- **Part A** – Model building (Decision Tree + Random Forest) with cost-sensitive analysis  
- **Part B** – Gradient Boosting vs Random Forest (conceptual comparison)  
- **Part C** – Interview preparation (theory + coding + debugging)  
- **Part D** – AI-assisted explanation of OOB error and evaluation  

---

##  Dataset

A synthetic dataset of **3000 insurance claims** was generated with the following features:

- claim_amount  
- num_previous_claims  
- policy_age  
- customer_age  
- num_dependents  
- fraud_score  

**Target Variable:**
- fraud (1 = Fraud, 0 = Not Fraud)

---

##  Workflow

1. Synthetic Data Generation  
2. Train-Test Split (80/20)  
3. Model Training:
   - Decision Tree (max_depth = 5)  
   - Random Forest (tuned using RandomizedSearchCV, optimized for recall)  
4. Model Evaluation:
   - Accuracy  
   - F1 Score  
   - ROC-AUC  
   - Recall (critical for fraud detection)  
5. Cost-Sensitive Evaluation:
   - False Negative (FN) cost = 10 × False Positive (FP)  

---

##  Decision Tree (Interpretability)

- Provides clear decision rules  
- Easy to explain to regulators  
- Useful for human review and auditing  

---

##  Random Forest (Performance)

- Reduces overfitting using ensemble learning  
- Optimized for **high recall** (important in fraud detection)  
- Better detection of fraudulent cases  

---

##  Cost-Sensitive Insight

- Missing a fraud (FN) is **10× more costly** than a false alarm (FP)  
- Random Forest minimizes total cost due to higher recall  
- Business decision is driven by **cost, not just accuracy**

---

##  Results

- Random Forest achieved higher recall and ROC-AUC  
- Decision Tree provided strong interpretability  
- Trade-off: Explainability vs Performance  

---

##  Deployment Recommendation

- Use **Random Forest** for automated fraud detection (high recall, better performance)  
- Use **Decision Tree** for explainability and regulatory compliance  
- Hybrid approach ensures both accuracy and interpretability  

---

##  Boosting vs Bagging (Part B)

| Aspect        | Random Forest (Bagging) | Gradient Boosting |
|--------------|------------------------|-------------------|
| Training     | Parallel               | Sequential        |
| Goal         | Reduce variance        | Reduce bias + variance |
| Speed        | Faster                 | Slower            |
| Overfitting  | Less prone             | Can overfit       |

---

##  AI-Augmented Insights (Part D)

### Topic: OOB (Out-of-Bag) Error

- OOB error acts like an internal validation method  
- Each data point is tested on trees where it was not used for training  

### Evaluation:
- AI explanation was intuitive but slightly simplified  
- Missing technical detail on how predictions are aggregated  

### Improvements:
- Added explanation of per-sample prediction  
- Clarified difference between OOB and test error  

---

##  Key Learnings

- Importance of recall in fraud detection  
- Cost-sensitive decision making  
- Bias-variance tradeoff in ensemble models  
- Difference between bagging and boosting  
- Understanding OOB error in Random Forest  

---

##  Tools & Libraries

- Python  
- NumPy  
- Pandas  
- Scikit-learn  
- Matplotlib  

---

##  How to Run

1. Open the notebook in Google Colab  
2. Run all cells sequentially  
3. Review model outputs and evaluation metrics  

---

##  Author

**Hiten Mistry**
