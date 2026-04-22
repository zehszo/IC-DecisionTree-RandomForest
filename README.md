# 🚢 Titanic Survival Prediction: Decision Trees & Random Forests

This repository contains a study developed during my Scientific Initiation (IC) research on tree-based classification models. The project explores the transition from simple **Decision Trees** to ensemble models (**Random Forests**), focusing on Feature Engineering, Hyperparameter Tuning, and the balance between model complexity and data noise.

## 📌 Project Objectives
* Implement and visualize Decision Tree structures.
* Evolve to Random Forests and optimize performance via `GridSearchCV`.
* Perform Feature Engineering to extract social signals from raw data.
* Analyze Feature Importance (MDI) and the impact of complexity on model generalization.

## 📊 Key Insights & Results

### 1. The Performance "Ceiling"
After a full pipeline of data treatment and optimization, the model reached a **final accuracy of 84.44%** on unseen test data. A central finding of this study was that while advanced techniques like `GridSearchCV` and complex feature creation were applied, the performance gains over the baseline were marginal. This reveals the unpredictable nature of the historical event, where chaos and unobserved factors impose a natural "predictive ceiling" on the dataset.

### 2. The Power of Social Class
The **Feature Importance (MDI)** analysis brought a valuable insight that challenges common intuition:
* In the baseline model, **`Pclass`** (Social Class) emerged as the most robust predictor, even surpassing gender (**`Sex`**).
* After Feature Engineering, variables such as **`Title`** (extracted from names) and **`Fare`** (purchasing power) took center stage.
* **Conclusion:** While the "women and children first" protocol was real, economic status and physical location on the ship were even more consistent mathematical filters for survival.

### 3. Feature Engineering vs. Complexity
New features such as `family_size`, `is_alone`, and `Title` were created. The process demonstrated that:
* The model is highly efficient at "cannibalizing" redundant variables: the `Title` feature absorbed much of the importance previously held by the `Sex` column.
* Extra complexity does not always translate into drastic performance jumps, reinforcing the principle that in Machine Learning, simplicity and a robust original signal are often the best allies for generalization.

## 🛠️ Technologies Used
* **Python**
* **Pandas / NumPy** (Data Manipulation)
* **Scikit-Learn** (Modeling, Pipeline, and GridSearchCV)
* **Matplotlib / Seaborn** (Data Visualization)

## 📁 Notebook Structure
1. **Exploratory Data Analysis:** Data cleaning and handling missing values.
2. **Baseline Establishment:** Training a Decision Tree and Random Forest with raw data.
3. **Feature Engineering:** Creating new attributes based on historical context.
4. **Optimization:** Hyperparameter tuning to mitigate overfitting.
5. **Final Evaluation:** Testing on unseen data and MDI importance analysis.

---
**Project developed by José Pedro** *Scientific Initiation - Exploring Predictive Models*
