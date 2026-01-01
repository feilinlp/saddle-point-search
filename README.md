# Reaction Path Optimization & String Method

## Overview
This repository contains a modular Python implementation of algorithms designed to identify Minimum Energy Paths (MEP) and saddle points between stable states. 

The project focuses on comparing standard optimization techniques (Gradient Descent, Newton's Method) against the **String Method**, applied to two distinct benchmark systems:
1.  **Müller-Brown Potential:** A standard 2D non-convex surface with multiple minima and saddle points.
2.  **Morse Potential Cluster (N=7):** A high-dimensional system representing the rearrangement of a 7-particle cluster.

## Features

### Supported Potentials
* **Müller-Brown:** 2D analytical potential using symbolic differentiation via `SymPy`.
* **Morse Cluster:** 7-particle system with translational/rotational invariance removal (11 degrees of freedom).

### Algorithms
* **Gradient Descent:** First-order optimization for finding local minima.
* **Newton's Method:** Second-order optimization using the Hessian matrix for faster convergence near minima.
* **Mixed Optimization:** A hybrid approach switching from Gradient Descent to Newton's Method.
* **Zero-Temperature String Method:** An algorithm for finding the Minimum Energy Path (MEP) connecting two minima in configuration space.

## Directory Structure

```text
├── src/
│   ├── potentials.py       # Physics models (MuellerBrown, MorseCluster)
│   ├── optimizers.py       # GD, Newton, and Mixed algorithms
│   ├── string_method.py    # String Method logic and initialization
│   └── visualization.py    # Plotting utilities for trajectories/energies
├── notebooks/              # Jupyter notebooks for running experiments
├── requirements.txt        # Python dependencies
└── README.md
