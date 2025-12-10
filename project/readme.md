# DS5020 Final Project — Linear Algebra & Probability for Data Science

This repository contains my individual final project for **DS5020**. 

## Due Date
**December 10, 2025 — 11:59 PM**

---

## Overview
Explore three complementary applications using real datasets:
1. **Prediction:** Housing price forecasting with regression and uncertainty *(Boston Housing dataset)*
2. **Perception:** Pattern recognition through dimensionality reduction *(Digits dataset)*
3. **Personalization:** Recommender systems and latent structure discovery *(MovieLens 100k dataset)*
---

## Project Goals
By completing this project, you will:
- Apply matrix representations, eigen decomposition, projections, and SVD to real data.
- Use probability to quantify uncertainty, model randomness, and interpret outcomes.
- Build a conceptual bridge between theory and AI/ML practice. :contentReference[oaicite:2]{index=2}

---

## Datasets
- **Boston Housing:** available via `scikit-learn` (and on Kaggle).
- **Digits:** built into `scikit-learn`.
- **MovieLens 100k:** available from GroupLens. :contentReference[oaicite:3]{index=3}

---

## Part I — Predictive Intelligence (Boston Housing)
**Theme:** Linear algebra as the engine of prediction.  
**Goal:** Use regression to predict housing prices and interpret uncertainty probabilistically.

### Tasks
- Load features as \( X \in \mathbb{R}^{n \times d} \) and targets as \( y \in \mathbb{R}^n \).
- Compute regression weights:
  \[
  \hat{w} = (X^\top X)^{-1} X^\top y
  \]
- Compute predictions \( \hat{y} = X\hat{w} \) and residuals \( r = y - \hat{y} \).
- Model residuals as Gaussian noise \( \epsilon \sim \mathcal{N}(0, \sigma^2) \) and estimate \( \sigma^2 \).
- Visualize:
  - True vs. predicted prices.
  - Histogram of residuals. :contentReference[oaicite:4]{index=4}

### Key Discussion Points
Explain how linear algebra enables prediction and how probability models uncertainty. :contentReference[oaicite:5]{index=5}

---

## Part II — Perceptual Intelligence (Digits)
**Theme:** Linear algebra as the language of perception.  
**Goal:** Use PCA to uncover structure in handwritten digits and apply probability for simple classification.

### Tasks
- Load the Digits dataset (each 8×8 image flattened to 64-D).
- Center data and compute covariance:
  \[
  C = \frac{1}{n-1} X^\top X
  \]
- Compute and sort eigenvalues/eigenvectors.
- Visualize top 10 eigenvectors (**eigendigits**).
- Project onto top \( k \) components and reconstruct images for different \( k \).
- Build a simple probabilistic classifier (e.g., Naïve Bayes) on reduced features; report accuracy. :contentReference[oaicite:6]{index=6}

### Key Discussion Points
Discuss how eigenvectors represent fundamental patterns and how probability governs decisions under uncertainty. :contentReference[oaicite:7]{index=7}

---

## Part III — Personalized Intelligence (MovieLens)
**Theme:** Linear algebra as the foundation of discovery and personalization.  
**Goal:** Use matrix factorization (SVD) to understand and predict preferences.

### Tasks
- Load a subset of MovieLens user–movie–rating data.
- Build rating matrix \( R \in \mathbb{R}^{m \times n} \) (handle missing values with zeros or averages).
- Perform truncated SVD:
  \[
  R \approx U_k \Sigma_k V_k^\top
  \]
- Interpret:
  - \( U_k \) as latent user preferences
  - \( V_k \) as latent movie features
- Predict missing ratings:
  \[
  \hat{R} = U_k \Sigma_k V_k^\top
  \]
- Experiment with different \( k \); compute reconstruction error \( \|R - \hat{R}\|_F \).
- Visualize latent representations in 2D. :contentReference[oaicite:8]{index=8}

### Key Discussion Points
Explain how linear algebra reveals hidden structure and how probability relates to uncertainty in recommendations. :contentReference[oaicite:9]{index=9}

---

## Integration & Reflection
Connect the three parts conceptually:

| Perspective | Mathematical Concept | AI/ML Analogy |
|------------|----------------------|---------------|
| Prediction | Linear regression, projection, Gaussian noise | Forecasting outcomes |
| Perception | Eigen decomposition, dimensionality reduction | Recognizing structure |
| Personalization | Matrix factorization, latent variables | Learning preferences |

### Questions to Address
1. How did linear algebra structure each problem?
2. How did probability help model uncertainty or belief?
3. How do these ideas together form the basis of intelligent systems?
4. Which part felt most intuitive or inspiring, and why? :contentReference[oaicite:10]{index=10}

---

## Deliverables
Submit:
- **Well-documented Jupyter Notebook** (or Python script) implementing all tasks with plots/results.
- **Final Project Report (PDF)** ≤ 10 pages.
- **Short Presentation** (8–10 minutes).
- **All source files** (`.ipynb`, `.py`, etc.). :contentReference[oaicite:11]{index=11}

---

## Evaluation Criteria
- **Final Report:** 35 marks  
- **Presentation:** 15 marks  
- **Technical/Analytical Execution:** 50 marks  
  - Part I: 15  
  - Part II: 15  
  - Part III: 15  
  - Integration & Reflection: 5 :contentReference[oaicite:12]{index=12}

---

## Suggested Repository Structure
```text
.
├── notebooks/
│   └── DS5020_FinalProject.ipynb
├── src/
│   ├── part1_regression.py
│   ├── part2_pca.py
│   └── part3_svd_recommender.py
├── data/
│   └── movielens_100k/   # if included locally
├── reports/
│   └── final_report.pdf
├── presentation/
│   └── final_presentation.pdf
└── README.md
