#  Breast Cancer Classification with Neural Network

A deep learning project that classifies breast tumors as **Malignant** or **Benign** using a Neural Network built with TensorFlow and Keras.

---

##  Overview

Breast cancer is one of the most common cancers worldwide. Early and accurate classification of tumors can significantly improve patient outcomes. This project applies a simple Neural Network on the **Wisconsin Breast Cancer Dataset** to predict whether a tumor is malignant or benign based on 30 cell nucleus features extracted from digitized images.

---

##  Project Structure

```
breast-cancer-classification/
│
├── DL_Project_1_Breast_Cancer_Classification_with_NN.ipynb  # Main notebook
├── data.csv                                                  # Dataset
└── README.md                                                 # Project documentation
```

---

##  Dataset

| Property        | Details                              |
|-----------------|--------------------------------------|
| Source          | Wisconsin Breast Cancer Dataset (sklearn) |
| Total Samples   | 569                                  |
| Features        | 30 numeric features                  |
| Target Classes  | Malignant (212) · Benign (357)       |
| Missing Values  | None                                 |

**Sample Features:** `radius_mean`, `texture_mean`, `perimeter_mean`, `area_mean`, `smoothness_mean`, `compactness_mean`, `concavity_mean`, and more.

> **Class Labels:** `0` → Malignant &nbsp;|&nbsp; `1` → Benign

---

##  Tech Stack

- **Language:** Python 3
- **Deep Learning:** TensorFlow · Keras
- **Data Processing:** NumPy · Pandas · Scikit-learn
- **Visualization:** Matplotlib

---

##  Model Architecture

```
Input Layer     →  30 features (Flatten)
Hidden Layer    →  20 neurons  (ReLU activation)
Output Layer    →  2 neurons   (Sigmoid activation)
```

**Training Config:**
- Optimizer: `Adam`
- Loss Function: `Sparse Categorical Crossentropy`
- Epochs: `10`
- Validation Split: `10%`

---

## 🔄 Workflow

1. **Data Collection** — Load dataset from `sklearn.datasets`
2. **Exploratory Analysis** — Shape, info, null checks, class distribution
3. **Preprocessing** — Feature/label split → Train/test split (80/20) → StandardScaler normalization
4. **Model Building** — Sequential Neural Network with TensorFlow/Keras
5. **Training** — Fit model with validation monitoring
6. **Evaluation** — Accuracy on test data, accuracy & loss curves
7. **Prediction** — Predictive system for new input data

---

##  Results

| Metric         | Value     |
|----------------|-----------|
| Training Split | 80%       |
| Test Split     | 20%       |
| Optimizer      | Adam      |
| Epochs         | 10        |

> Training and validation accuracy/loss curves are visualized in the notebook.

---

##  Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/breast-cancer-classification.git
cd breast-cancer-classification
```

### 2. Install dependencies
```bash
pip install numpy pandas matplotlib scikit-learn tensorflow
```

### 3. Run the notebook
```bash
jupyter notebook DL_Project_1_Breast_Cancer_Classification_with_NN.ipynb
```

---

##  Making a Prediction

The notebook includes a **predictive system** at the end. You can pass raw tumor measurements and get a diagnosis:

```python
input_data = (11.76, 21.6, 74.72, 427.9, 0.08637, ...)  # 30 features

# Output
# → 'The tumor is Benign'  or  'The tumor is Malignant'
```

---

##  Future Improvements

- [ ] Try deeper architectures (more hidden layers)
- [ ] Experiment with different optimizers and learning rates
- [ ] Add confusion matrix and classification report
- [ ] Deploy as a web app using Streamlit or Flask
- [ ] Hyperparameter tuning with Keras Tuner

---

##  Author

**Rohith**  
Aspiring Data Scientist | Deep Learning Enthusiast  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/your-profile)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/your-username)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
