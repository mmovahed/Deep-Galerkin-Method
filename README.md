# Deep Galerkin Method (DGM)

## Overview
This repository provides implementations of the **Deep Galerkin Method (DGM)** for solving differential equations using deep learning. The method is an extension of traditional numerical techniques such as the finite element method (FEM) and the collocation method, where the residuals of partial differential equations (PDEs) are weighted using test functions to improve stability and accuracy.

## Implemented Examples
This repository includes implementations for the following differential equations:

1. **Ordinary Differential Equation (ODE):**
   - Solving the first-order equation \( $\frac{dy}{dx} = y$ \) using Deep Galerkin.
   - The exact solution is \( $y = e^x$ \).
   - The neural network approximates the solution by minimizing a loss function that integrates the PDE residuals weighted by a test function.

2. **Partial Differential Equation (PDE) - Heat Equation:**
   - Solving the heat equation: \( $\frac{\partial u}{\partial t} = \alpha \frac{\partial^2 u}{\partial x^2}$ \).
   - The exact solution is \( $u(x,t) = e^{-\alpha \pi^2 t} \sin(\pi x)$ \).
   - The neural network minimizes the residual error of the PDE while enforcing boundary and initial conditions.

## Installation
To run the examples, install the required dependencies using:
```sh
pip install torch numpy matplotlib
```

## Results
For both examples, the learned solution is compared with the exact analytical solution, and the Mean Absolute Error (MAE) is computed to measure accuracy. 3D plots visualize the network's approximation and the exact solution.

## Contributions
Feel free to contribute by improving the implementation, adding more PDEs, or optimizing training strategies. Open a pull request if you have an enhancement.

## License
This project is licensed under the MIT License.
