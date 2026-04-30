# Machine_Learning_Assignment1
-------
# 📘 Bias–Variance Trade-off using Polynomial Regression

## 🎯 Objective
The objective of this experiment is to analyze the **bias–variance trade-off** in machine learning using polynomial regression models of different complexities. We study how model performance changes with increasing complexity using multiple training datasets.

---

## 📊 Dataset Description

We generate synthetic data using a noisy sine function:

\[
y = \sin(2\pi x) + \epsilon
\]

Where:
- \( x \in [1, 3] \)
- \( \epsilon \sim \mathcal{N}(0, \sigma^2) \) (Gaussian noise)

### Dataset settings:
- 20 different training datasets
- 25 samples per dataset
- Noise standard deviation = 0.25
- Fixed test dataset for evaluation

---

## 🧠 Model Description

We use **Polynomial Regression**, where input features are transformed into polynomial form:

\[
\phi(x) = [1, x, x^2, x^3, ..., x^d]
\]

The model is trained using the **closed-form solution (Normal Equation)**:

\[
w = (X^T X)^{-1} X^T y
\]

### Polynomial degrees tested:
- Degree 1 (Linear model)
- Degree 4 (Moderate complexity)
- Degree 6 (High complexity)
- Degree 9 (Very high complexity)

---

## 🔁 Experimental Procedure

For each polynomial degree:

1. Generate 20 different training datasets  
2. Train polynomial regression model on each dataset  
3. Predict outputs on a fixed test set  
4. Store all predictions  
5. Compute:
   - Mean prediction  
   - Bias²  
   - Variance  
6. Visualize:
   - All model predictions  
   - True function  
   - Mean prediction  

---

## 📐 Bias and Variance Formulation

### 🔴 Bias²
Measures how far the average prediction is from the true function:

\[
\text{Bias}^2 = \mathbb{E}[(\bar{f}(x) - f(x))^2]
\]

---

### 🔵 Variance
Measures how much predictions vary across datasets:

\[
\text{Variance} = \mathbb{E}[(f_i(x) - \bar{f}(x))^2]
\]

---

## 📈 Results

### Degree 1
- High bias  
- Low variance  
- Underfitting occurs  

---

### Degree 4
- Medium bias  
- Medium variance  
- Balanced model  

---

### Degree 6
- Low bias  
- Higher variance  
- Good fit with slight instability  

---

### Degree 9
- Very low bias  
- Very high variance  
- Overfitting occurs  

---

## 📊 Summary Table

| Degree | Bias | Variance | Interpretation |
|--------|------|----------|---------------|
| 1 | High | Low | Underfitting |
| 4 | Medium | Medium | Balanced |
| 6 | Low | High | Slight overfitting |
| 9 | Very Low | Very High | Overfitting |

---

## 📉 Bias–Variance Trade-off

- Increasing model complexity reduces bias  
- Increasing model complexity increases variance  
- There is a trade-off between bias and variance  
- Optimal performance occurs at a balanced complexity level  

---

## 🧾 Conclusion

This experiment demonstrates the **bias–variance trade-off** in machine learning:

- Simple models → High bias, low variance  
- Complex models → Low bias, high variance  

The best model is the one that achieves a balance between both, minimizing total prediction error.

---

## 🧠 Key Insight

> As model complexity increases, bias decreases while variance increases. The goal is to find an optimal trade-off between them.

---
