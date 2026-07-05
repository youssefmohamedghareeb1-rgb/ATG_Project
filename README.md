# Acid-Mediated Tumor Growth (ATG) Modeling 🔬💻

Cancer invasion is strongly influenced by interactions between tumor cells and their surrounding microenvironment. One crucial mechanism is the production of excess acid by tumor cells, which damages healthy tissue and promotes tumor expansion. 

This repository contains the computational implementation of the **Acid-Mediated Tumor Growth (ATG) model**. It uses a coupled system of reaction-diffusion Partial Differential Equations (PDEs) to simulate the dynamics of normal cells, tumor cells, and extracellular acid concentration.

## 🌟 Key Features & Methodology

This project approaches the ATG model from two distinct computational angles:

### 1. Traditional Numerical Methods
We implemented six robust numerical schemes combining various spatial discretization and time integration techniques:
* **Spatial Discretization:** Finite Volume Method (FVM), Finite Difference Method (FDM), and Finite Element Method (FEM).
* **Time Integration:** Explicit Fourth-Order Runge–Kutta (RK4) and Implicit Crank-Nicolson.
* *Finding:* Implicit Crank-Nicolson methods significantly reduced computational cost compared to explicit schemes while maintaining stability.

### 2. Scientific Machine Learning (SciML)
To bypass the heavy computational load of traditional solvers, we developed two machine learning models to approximate the PDE system's solutions:
* **Deep Neural Network (DNN):** A surrogate model trained on numerical data, achieving exceptional prediction accuracy with a final loss of **$4.73 \times 10^{-8}$**.
* **Physics-Informed Neural Network (PINN):** An advanced AI approach that successfully recovered the model dynamics purely through the underlying physics, without requiring labeled training data.

## 📊 Results

Both the DNN and PINN models successfully reproduced the spatial evolution of:
- Normal cell density
- Tumor cell density
- Acid concentration / pH levels

The machine learning models showed excellent agreement with the traditional numerical solutions, demonstrating their effectiveness as highly efficient alternatives for solving complex biomedical reaction-diffusion systems.

## 🛠️ Technologies Used
* **Mathematics:** Partial Differential Equations (PDEs), Method of Lines
* **Numerical Analysis:** FVM, FDM, FEM, RK4, Crank-Nicolson
* **Machine Learning:** Deep Neural Networks (DNNs), Physics-Informed Neural Networks (PINNs)
* **Domain:** Scientific Machine Learning (SciML), Biomedical Engineering, Computational Oncology

---
*This project was developed to explore efficient computational alternatives for predictive oncology and complex biological system modeling.*
