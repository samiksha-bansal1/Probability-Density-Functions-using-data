# Assignment 3: Probability Density Function (PDF) Estimation

This repository contains the implementation for Assignment 3, focusing on parameter estimation for the NO2 feature from the India Air Quality dataset. The project applies a non-linear transformation to the data based on a university roll number and estimates the parameters of the resulting probability distribution.

## Dataset
* **Feature:** NO2 (Nitrogen Dioxide)
* **Source:** [India Air Quality Data (Kaggle)](https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data)

## Project Objective
The goal is to transform the original air quality feature $x$ into a new variable $z$ and fit a Gaussian-like density function:

$$\hat{p}(z) = c \cdot e^{-\lambda (z - \mu)^2}$$

The objective is to determine the optimal values for the parameters $(\lambda, \mu, c)$ that best represent the distribution of the transformed data.

## Methodology

### 1. Data Transformation
The original feature $x$ is transformed into $z$ using the following roll-number-dependent function:
$$z = x + a_r \cdot \sin(b_r \cdot x)$$

**Transformation Coefficients:**
* $a_r = 0.05 \times (r \pmod 7)$
* $b_r = 0.3 \times ((r \pmod 5) + 1)$
* $r$: Roll Number (**102317096**)

### 2. Parameter Calculation
For the roll number **102317096**, the calculated transformation coefficients are:
* **$a_r$**: 0.0
* **$b_r$**: 0.6

## Results
After applying the transformation and fitting the model using `scipy.optimize.curve_fit`, the following parameters were estimated:

| Parameter | Estimated Value | Description |
| :--- | :--- | :--- |
| **$\mu$** | 20.0482684 | Mean of the transformed data |
| **$\lambda$** | 0.0034142 | Distribution spread (precision factor) |
| **$c$** | 0.0321697 | Normalization constant |

**Author:** Samiksha  
**Roll Number:** 102317096
