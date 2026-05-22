# Subsystem QFI and Scrambling Dynamics in Critical Systems

This repository contains the numerical implementation associated with the published project on quantum metrology, information scrambling, and critical dynamics in many-body quantum systems.

The main notebook, `subsystem qfi scrambling.ipynb`, studies how local subsystems of a scrambling quantum system can act as effective quantum stopwatches. The workflow follows the framework developed in the paper:

**Quantum timekeeping and the dynamics of scrambling in critical systems**  
Devjyoti Tripathy, Federico Centrone, and Sebastian Deffner  
arXiv:2603.13016  
https://arxiv.org/abs/2603.13016

## Overview

The project investigates the connection between subsystem quantum Fisher information (QFI), out-of-time-ordered correlators (OTOCs), and scrambling dynamics near criticality. The key idea is that the reduced state of a local subsystem encodes time through its increasing distinguishability from the initial preparation, allowing scrambling dynamics to be interpreted through a quantum-metrological lens.

## Main Features

The notebook includes:

- Construction of a chaotic transverse-field Ising spin-chain Hamiltonian
- Ground-state preparation across different transverse-field values
- Crank–Nicolson time evolution for many-body quantum dynamics
- Computation of subsystem QFI as a function of field strength and time
- Computation of OTOC dynamics over the same parameter regime
- Extraction of Lyapunov-like exponents from OTOC decay
- Construction of Fisher–Lyapunov bound heatmaps
- Visualization of QFI, OTOC, and scrambling-bound behavior near criticality

## Model

The simulated spin-chain Hamiltonian includes nearest-neighbor Ising interactions, transverse and longitudinal fields, and an additional interaction term used to probe chaotic/non-integrable dynamics:

```math
H =
-J \sum_i \sigma_i^z \sigma_{i+1}^z
-h \sum_i \sigma_i^x
-g \sum_i \sigma_i^z
-J_2 \sum_i \sigma_i^z \sigma_{i+2}^z .
```

This model provides a controlled numerical setting for studying how scrambling, subsystem distinguishability, and critical amplification are related.

## Repository Structure

- `subsystem qfi scrambling.ipynb` — main simulation notebook
- generated figures/outputs — QFI heatmaps, OTOC heatmaps, Lyapunov-exponent plots, and Fisher–Lyapunov bound visualizations, if saved during execution

## Dependencies

The notebook uses:

- Python
- NumPy
- SciPy
- Matplotlib
- QuTiP

## Citation

If you use this code or build on this project, please cite:

```bibtex
@article{tripathy2026quantum,
  title={Quantum timekeeping and the dynamics of scrambling in critical systems},
  author={Tripathy, Devjyoti and Centrone, Federico and Deffner, Sebastian},
  journal={arXiv preprint arXiv:2603.13016},
  year={2026},
  doi={10.48550/arXiv.2603.13016}
}
```
