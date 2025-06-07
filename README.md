# SVM-model

This project demonstrates how to apply Support Vector Machines (SVM) for binary classification using the Breast Cancer Wisconsin dataset. Both linear and non-linear (RBF kernel) SVMs are implemented and evaluated.

---

##  Dataset

- **Dataset**: Breast Cancer Wisconsin (Diagnostic)
- **Target Variable**: `diagnosis` (0 = Benign, 1 = Malignant)
- **Features**: 30 numerical features extracted from cell nuclei images.
- **Total Records**: 569

---

##  Libraries Used

- `pandas`, `numpy`
- `scikit-learn`
- `matplotlib`, `seaborn`

---

##  Project Workflow

1. **Data Preprocessing**
   - Dropped `id` column
   - Label encoded the target (`M` → 1, `B` → 0)
   - Standardized features using `StandardScaler`
   - Split dataset into training and testing sets (80/20 split)

2. **Model Training**
   - Trained a **Linear SVM** classifier
   - Trained a **Non-linear SVM** with **RBF kernel**

3. **Hyperparameter Tuning**
   - Used `GridSearchCV` to find the best `C` and `gamma` values for the RBF kernel

4. **Evaluation**
   - Evaluated using precision, recall, F1-score, and accuracy
   - Performed 5-fold cross-validation
   - Visualized decision boundaries using PCA

---

## Results

### Linear SVM

| Metric      | Class 0 | Class 1 |
|-------------|---------|---------|
| Precision   | 0.95    | 1.00    |
| Recall      | 1.00    | 0.90    |
| F1-Score    | 0.97    | 0.95    |
| **Accuracy**| **96%** |

---

### RBF SVM

| Metric      | Class 0 | Class 1 |
|-------------|---------|---------|
| Precision   | 0.96    | 1.00    |
| Recall      | 1.00    | 0.93    |
| F1-Score    | 0.98    | 0.96    |
| **Accuracy**| **97%** |

---

###  Best Hyperparameters from Grid Search

```text
{'C': 1, 'gamma': 'scale', 'kernel': 'rbf'}
