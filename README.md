# UCS654 Predictive Analysis Using Statistics
## Assignment-1
## Learning Probability Density Functions using Roll-Number-Parameterized Non-Linear Model

# 1. Introduction
``` text
 This assignment focuses on understanding probability density functions by working with real air quality data. A nonlinear mathematical transformation is applied to the data, and the parameters of the resulting distribution are learned. To make each student’s work unique, the transformation is defined using the university roll number.
```

## 2. Dataset Information
```text
Dataset Name : India Air Quality Dataset (Kaggle)
Feature Used : Nitrogen Dioxide (NO₂)
Symbol       : x
Preprocessing:
- Removed missing values
- Removed invalid entries
```
## 3. Approach and Method
The overall approach consists of two main stages as described below.

## Step 1: Nonlinear Transformation Based on Roll Number

Each NO₂ data value **x** is converted into a new value **z** using a nonlinear equation:

```text
z = x + a_r · sin⁻¹(b_r · x)
The parameters a_r and b_r are calculated from the university roll number r using the following formulas:

a_r = 0.05 × (r mod 7)
b_r = 0.3 × (r mod 5 + 1)
For my roll number, the computed parameter values are:
Parameter	Computed Value
a_r	0.15000000000000002
b_r	1.5

Since the inverse sine function is valid only for values between -1 and 1, the transformation is applied only to those data points that satisfy:
-1 ≤ b_r · x ≤ 1
This condition ensures that the transformation remains mathematically valid
```

