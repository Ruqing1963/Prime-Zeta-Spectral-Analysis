![Status](https://img.shields.io/badge/Status-Accepted_for_Publication-success)
![License](https://img.shields.io/badge/License-MIT-blue)

# Numerical Investigation of Spectral Correlations between Prime Number Distribution and Riemann Zeta Zeros

This repository contains the source code and datasets for the paper: **"Numerical Investigation of Spectral Correlations between Prime Number Distribution and Riemann Zeta Zeros"**.

## 📄 Abstract

We present an exploratory data analysis concerning the local distribution of prime numbers and their correlation with the imaginary parts of Riemann zeta zeros ($\gamma_n$). Through large-scale numerical simulations ($N=1.5 \times 10^8$), we evaluate a heuristic capture model derived from the Explicit Formula. Our analysis reveals three distinct regimes: (1) a **Correlation Regime** where a dual-frequency model enhances prime detection; (2) a **Divergence Regime** driven by cumulative phase errors; and (3) a recovery phase via **Iterative Correction**.

A rigorous **True Null Model** validation (randomized phases, $M=10,000$) confirms that the observed spectral correlations are statistically significant ($p < 10^{-4}$), providing strong evidence that the signal arises from the intrinsic phase information of the Riemann zeros.

## 📂 Repository Structure

* **`Fig1_coherence.csv`**: Raw data for the "Correlation Regime" analysis. Contains Prime Yield comparison between Single-Frequency and Dual-Frequency models.
* **`Fig2_drift.csv`**: Data demonstrating the Phase Divergence phenomenon and error accumulation.
* **`Fig3_relay.csv`**: Data for the Iterative Correction strategy.
* **`NullModel_Validation.py`**: Python script used to perform the permutation test (True Null Model).
* **`Capture_Function.py`** (Optional): The core algorithm implementation.

## ⚙️ Methodology & Parameters

To ensure reproducibility and rule out parameter tuning (overfitting), the capture function parameters were **fixed** based on theoretical derivation:

* **Phases ($\phi_n$):** Fixed at `0.0` (Consistent with the theoretical real part of Riemann terms, $\cos(\gamma \ln x)$).
* **Amplitude ($A$):** `2.0` (Normalization constant).
* **Damping ($\zeta$):** `0.1` (Empirical choice for SNR optimization).

## 🚀 How to Reproduce

### 1. Install dependencies
```bash
pip install numpy pandas matplotlib seaborn scipy

