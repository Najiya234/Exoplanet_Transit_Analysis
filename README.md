# Exoplanet Transit Analysis

## Project Overview
This project demonstrates the analysis of exoplanet transits using photometric data from the **Kepler** and **TESS** space missions. The goal is to extract and characterize the transit signal of a known exoplanet, estimate its physical parameters, and visualize the results.

---

## Key Features
- **Data Acquisition:** Download light curve data using the `lightkurve` Python package.  
- **Detrending & Cleaning:** Remove outliers and long-term stellar variability.  
- **Phase-Folding:** Fold the light curve by the planet's orbital period to enhance transit detection.  
- **Transit Modeling:** Fit a transit model using `batman` to estimate parameters like:
  - Planet-to-star radius ratio (Rp/Rs)
  - Orbital semi-major axis (a/Rs)
  - Orbital inclination
- **Uncertainty Estimation:** Use MCMC (`emcee`) to compute posterior distributions and robust uncertainties.  
- **Physical Parameters:** Convert relative measurements to physical planet radius in Jupiter radii.  
- **Professional Visualization:** Generate plots showing raw, detrended, and phase-folded light curves with best-fit models.

---

## Workflow Steps
1. **Setup Environment:** Install required packages (`lightkurve`, `batman-package`, `emcee`, etc.).  
2. **Download Data:** Search and download light curves for a target exoplanet.  
3. **Clean & Detrend:** Remove outliers and flatten the light curve.  
4. **Fold Light Curve:** Fold by known period to reveal transit signals.  
5. **Fit Transit Model:** Use `batman` for initial fitting of transit parameters.  
6. **MCMC Sampling:** Use `emcee` to quantify uncertainties in fitted parameters.  
7. **Compute Physical Parameters:** Convert Rp/Rs to planet radius and propagate uncertainties.  
8. **Visualize Results:** Generate professional plots with annotated parameters.  

---

## Getting Started

### Requirements
- Python 3.8+  
- Packages: `lightkurve`, `batman-package`, `emcee`, `corner`, `matplotlib`, `numpy`  

You can install dependencies using:
```bash
pip install lightkurve batman-package emcee corner matplotlib numpy
