# Assignment-3: Learning Probability Density Functions

This repository contains **Assignment-3** for learning **Probability Density Functions (PDFs)** using a roll-number-based non-linear transformation of the NO2 air quality feature.

---

## Dataset
- Feature: **NO2**
- Source: [India Air Quality Data - Kaggle](https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data)

---

## Objective
- Transform the NO2 values using a **roll-number-dependent function**.  
- Estimate the parameters of a Gaussian-like probability density function:  

$$
\hat{p}(z) = c \cdot e^{-\lambda (z - \mu)^2}
$$

- Submit the estimated parameters (λ, μ, c).

---

## Transformation Formula
The feature `x` is transformed into `z` using:

$$
z = x + a_r \cdot \sin(b_r \cdot x)
$$

Where:  
- `a_r = 0.05 × (r mod 7)`  
- `b_r = 0.3 × ((r mod 5) + 1)`  
- `r` = your **university roll number**  
- `mod` means the remainder after division

---

## Usage
1. Open `Assignment-3 (Probability Density Function).ipynb` in Jupyter Notebook.  
2. Replace `r` with your roll number.  
3. Run the notebook to transform the data, estimate PDF parameters, and visualize results.  

---

**Author:** Samiksha  
**Roll Number:** 102317096
