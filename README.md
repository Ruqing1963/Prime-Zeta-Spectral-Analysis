# Numerical Investigation of Spectral Correlations between Prime Number Distribution and Riemann Zeta Zeros

This repository contains the source code and datasets for the paper: **"Numerical Investigation of Spectral Correlations between Prime Number Distribution and Riemann Zeta Zeros"**.

## 📄 Abstract
We present an exploratory data analysis concerning the local distribution of prime numbers and their correlation with the imaginary parts of Riemann zeta zeros. Through large-scale numerical simulations ($N=1.5 \times 10^8$), we evaluate a heuristic capture model derived from the Explicit Formula. The results define a "Correlation Regime" and validatethe statistical significance using a True Null Model ($p < 10^{-4}$).

## 📂 Repository Structure

- **`Fig1_coherence.csv`**: Raw data for the "Correlation Regime" analysis. Contains Prime Yield comparison between Single-Frequency and Dual-Frequency models.
- **`Fig2_drift.csv`**: Data demonstrating the Phase Divergence phenomenon and error accumulation.
- **`Fig3_relay.csv`**: Data for the Iterative Correction strategy.
- **`NullModel_Validation.py`**: Python script used to perform the permutation test (True Null Model).
- **`Capture_Function.py`** (Optional): The core algorithm implementation.

## ⚙️ Methodology & Parameters

As stated in the manuscript, the capture function parameters were **fixed** based on theoretical derivation, not tuned:
* **Phases ($\phi_n$):** Fixed at `0.0` (Consistent with $\cos(\gamma \ln x)$).
* **Amplitude ($A$):** `2.0`
* **Damping ($\zeta$):** `0.1`

## 🚀 How to Reproduce

1. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib seaborn scipy
