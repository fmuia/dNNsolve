# dNNsolve: An Enhanced Dual Neural Network-based PDE Solver

## Overview
This repository is associated with the paper "dNNsolve: An Efficient NN-based PDE Solver," where we introduce a novel dual Neural Network (dNN) approach for solving a broad spectrum of Ordinary and Partial Differential Equations (ODEs/PDEs) effectively. The approach builds upon the concept of Physics Informed Neural Networks (PINNs) introduced by Raissi et al. (2017) in their foundational papers (arXiv:1711.10561 and arXiv:1711.10566), which redefine the solving of differential equations as an optimization problem where a neural network minimizes a loss function reflecting the PDE and its boundary conditions.

## Main Features
- **Dual Activation Functions:** Utilizes both sine and sigmoidal activation functions to efficiently capture secular and periodic patterns in the solutions, addressing one of the main limitations of traditional PINNs which typically use a single type of activation function.
- **Minimized Hyperparameter Tuning:** Unlike traditional PINN implementations that require extensive hyperparameter tuning, dNNsolve significantly reduces the need for this, simplifying the user experience and enhancing reproducibility.
- **Enhanced Generalizability:** Through its architecture, dNNsolve demonstrates superior adaptability across different types of PDEs without manual intervention for each new equation type.

## Repository Structure
Each folder within this repository contains results from various runs using the dNNsolve architecture, detailing the efficiency and accuracy of the model across different settings:
- `Main1D.ipynb`, `Main2D.ipynb`, `Main3D.ipynb`: Main notebooks for solving equations in 1D, 2D, and 3D.
- `auxiliary_func_noprint.ipynb`: Auxiliary functions used in notebooks without print statements.
- `1D_randomMiniBatch_ADAM_epochs=1000/`: Results from 1D problem instances using 1000 epochs with ADAM optimizer and random mini-batches. Contains files such as `1to1_results_randomMiniBatch.txt` detailing outcomes like epochs, total time, losses, and mean squared error estimates.
- `ADAM_epochs=200/`, `ADAM_epochs=400/`: Contains similar result files for runs with specified numbers of epochs.
- `README.md`: This README file.

## Research Impact
This implementation extends the foundational work on PINNs by introducing methodologies that alleviate some of the known challenges such as the need for extensive hyperparameter tuning and the reliance on specific activation functions which may not generalize across all types of differential equations.

## References
Please refer to our paper for detailed methodology and comparisons:

Title: dNNsolve: An Efficient NN-based PDE Solver,
Authors: V. Guidetti (DESY), F. Muia (DESY and University of Cambridge), Y. Welling (DESY), A. Westphal (DESY)
arXiv: 2103.08662

**Original PINN Papers**:
  - M. Raissi et al., "Physics informed deep learning (Part I): Data-driven solutions of nonlinear partial differential equations" [arXiv:1711.10561].
  - M. Raissi et al., "Physics informed deep learning (Part II): Data-driven discovery of nonlinear partial differential equations" [arXiv:1711.10566].

## Contacts
For further information or queries, please contact:
- Veronica Guidetti - veronica.guidetti@desy.de
- Francesco Muia - fm538@cam.ac.uk
- Yvette Welling - yvette.welling@desy.de
- Alexander Westphal - alexander.westphal@desy.de
