# Assignment 01 – Linear Classifiers

## Problem Statement
Consider a two-class database with the following properties:

- The data follow a normal (Gaussian) distribution
- Class means:
  - Class 1: μ₁ᵀ = [2, 2]
  - Class 2: μ₂ᵀ = [0, 0]
- Equal variance for both classes:
  - σ₁² = σ₂² = 2

Using the following classifiers:
- Perceptron
- Least Squares
- Support Vector Machine (SVM)

Compare their performance under different training data proportions:
- 50% training, 50% test
- 30% training, 50% test
- 10% training, 50% test

---

## Methodology

1. **Dataset Generation**
   - Synthetic data were generated using multivariate Gaussian distributions.
   - Labels were assigned as:
     - Class 1 → +1
     - Class 2 → −1

2. **Train/Test Splits**
   - Three different training sizes were evaluated.
   - Test data was fixed at 50% to ensure fair comparison.

3. **Models Implemented**
   - Perceptron (online learning, misclassification-based updates)
   - Least Squares classifier (global squared error minimization)
   - Linear SVM (margin maximization)

4. **Evaluation Metric**
   - Classification accuracy on the test set.

---

## Results Summary

| Training % | Perceptron | Least Squares | SVM |
|-----------:|-----------:|--------------:|----:|
| 50% | 0.795 | 0.865 | 0.855 |
| 30% | 0.835 | 0.855 | 0.845 |
| 10% | 0.865 | 0.850 | 0.860 |

---

## Observations

- The **Perceptron** shows unstable generalization performance due to sensitivity to sample order and noisy boundary points.
- The **Least Squares** classifier provides stable performance across different training sizes.
- The **SVM** demonstrates strong generalization, especially when training data is limited, due to margin maximization.

---

## Conclusion

This experiment highlights the impact of learning objectives on classifier performance. While the perceptron is simple and intuitive, Least Squares and SVM provide more robust and reliable performance, particularly in limited-data scenarios.

