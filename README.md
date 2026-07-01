# Bayesian Sensor Fusion and Gaussian Process Mapping for Human–Robot Collaborative Hygiene Monitoring and Surface Disinfection

## Overview

This repository contains the research, mathematical modeling, and MATLAB implementation for a probabilistic framework for human–robot collaborative hygiene monitoring and autonomous surface disinfection.

The project integrates Bayesian Sensor Fusion with Gaussian Process Mapping to estimate surface contamination, quantify uncertainty, and generate intelligent disinfection decisions. The proposed framework is implemented and evaluated in MATLAB, where its performance is compared against an Extended Kalman Filter (EKF)-based approach.

## Project Objectives

- Develop a Bayesian multi-sensor fusion framework for contamination estimation.
- Model spatial contamination using Gaussian Process Regression.
- Quantify uncertainty in contamination predictions.
- Compare Bayesian-GP mapping with an Extended Kalman Filter implementation.
- Evaluate estimation accuracy and robustness for robotic hygiene monitoring.

## Methodology

The project consists of:

- Mathematical formulation of Bayesian Sensor Fusion
- Gaussian Process Regression for probabilistic hygiene mapping
- Extended Kalman Filter (EKF) implementation for comparison
- MATLAB simulation and analysis
- Performance comparison using estimation accuracy and uncertainty metrics

## Results

Analytical validation and MATLAB simulation on a representative 3×3 surface-patch grid show:

- **91.8%** reduction in estimation uncertainty vs. prior belief
- **81.6%** improvement over RGB-D-only estimation
- **~8.1%** lower estimation error (MSE) vs. the EKF baseline
- **9/9** full spatial coverage vs. **5/9** for EKF and other non-spatial baselines
- EKF, designed for time-series tracking, cannot propagate estimates to unobserved patches; GP's explicit spatial correlation modeling is what enables full-surface coverage with calibrated uncertainty

*Note: these results are analytical and simulation-based, not from physical hardware trials.*

## Repository Contents

| Folder | Description |
|---|---|
| `docs/` | Report documentation, presentations, one-page proposal, and bibliography report |
| `matlab/` | MATLAB implementation |
| `results/` | Simulation results and figures |
| `images/` | Plots and visualizations |
| `README.md` | This file |

## Technologies

- MATLAB
- Bayesian Statistics
- Gaussian Process Regression
- Extended Kalman Filter (EKF)
- Probabilistic Robotics
- Human–Robot Collaboration

## Status

Framework validated analytically and via MATLAB simulation on a representative case study. Next steps include ROS 2 integration, Gazebo simulation, and hardware validation on a mobile manipulator platform.

## Author & Acknowledgements

**Team:** Alwa Jyoshna, Kappala Mahesh, Vallepu Vishnu
**Course:** M.Eng. in Robotics, Technische Hochschule Deggendorf
**Supervisor:** Prof. Dr.-Ing. Hamidreza Heidari

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
