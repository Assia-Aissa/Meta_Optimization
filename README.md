

#  Meta-Optimization of Optimizers for Time Series Forecasting with Bayesian Optimization

> Hyperparameter tuning for Adam, SGD, and RMSprop using Bayesian Optimization for LSTM-based time series forecasting.

##  Project Overview

This project explores **meta-optimization** techniques to fine-tune the hyperparameters of three popular optimizers—**Adam**, **SGD**, and **RMSprop**—used in training **LSTM** models for time series prediction.

We leverage **Bayesian Optimization** to intelligently search the hyperparameter space (learning rate, momentum, etc.), aiming to:

- Improve model accuracy
- Speed up convergence
- Enhance training stability

### 🧪 Tested on:
- Real-world **Weather dataset** (from Kaggle)
- LSTM model architecture for **univariate time series forecasting**

---

## 🛠️ Methods & Technologies

| Component       | Description |
|----------------|-------------|
| **Model**       | LSTM (Stacked) |
| **Optimizers**  | Adam, SGD, RMSprop |
| **Meta-Optimization** | Bayesian Optimization (with Scikit-Optimize) |
| **Evaluation Metrics** | MAE (Mean Absolute Error), training time, convergence |

---

## 📊 Key Results

| Optimizer | MAE Initial | MAE After BO | Improvement |
|----------|-------------|--------------|-------------|
| **Adam** | 0.6269      | 0.5277       | +15.8%      |
| **SGD**  | 0.7440      | 0.5372       | +27.8%      |
| **RMSprop** | 0.5721  | 0.5213       | +8.9%       |

- **SGD** became the best performer after tuning, despite being the worst before.
- **Bayesian Optimization** effectively reduced error and stabilized training.
- **Visualizations** showed clear improvement in learning curves and predictions.


---

## 🔍 Hyperparameters Tuned

### 📌 Adam
- `learning_rate ∈ [1e-5, 1e-2]`
- `beta_1 ∈ [0.8, 0.99]`
- `beta_2 ∈ [0.9, 0.999]`

### 📌 SGD
- `learning_rate ∈ [1e-4, 1e-1]`
- `momentum ∈ [0.5, 0.99]`

### 📌 RMSprop
- `learning_rate ∈ [1e-5, 1e-2]`
- `rho ∈ [0.8, 0.99]`

---

## 📈 Model Architecture (LSTM)

- 2 LSTM layers: 64 and 32 units
- Dropout: 0.2
- Loss Function: MAE
- Output: 1-step prediction (Dense layer)

---

## 📁 Repository Structure

```bash
.
├── meta_optimisation.ipynb        
├── Météo.csv 
├── README.md                    
