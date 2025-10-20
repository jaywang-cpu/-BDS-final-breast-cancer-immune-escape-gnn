#  PD-1/PD-L1 Immune Checkpoint Pathway Gene Expression Prediction System

##  Project Overview

This project develops a machine learning-based prediction system for **PDCD1 (PD-1) expression levels** using immune checkpoint pathway-related genes in breast cancer patients. The core objective is to **quantify immune escape risk** and provide personalized immunotherapy treatment guidance.

### 🔬 Core Scientific Hypothesis
**Higher PD-1/PD-L1 pathway expression → Stronger immune suppression → Higher tumor immune escape risk → Paradoxically better response to immune checkpoint inhibitors**

##  Methodology

### Data Source
- **Cancer Type**: Breast Cancer (BRCA)
- **Sample Size**: 24 patients
- **Gene Panel**: 5 key immune checkpoint pathway genes
  - `PDCD1` (PD-1 receptor) - Target prediction gene
  - `CD274` (PD-L1) - Most important predictor (43.9% weight)
  - `CD8A` (T-cell marker) - 23.9% weight
  - `PRF1` (Perforin) - 10.5% weight
  - `IFNG` (Interferon-γ) - 8.4% weight
  - `GZMB` (Granzyme B) - 7.9% weight

###  Machine Learning Pipeline
1. **Feature Engineering**: Multi-gene weighted scoring system
2. **Model Selection**: RandomForest (optimal performance)
3. **Risk Stratification**: Binary classification (High/Low expression)
4. **Validation**: Cross-validation with multiple algorithms
5. **Clinical Translation**: Interactive prediction interface

##  Key Results

### Model Performance
- **Algorithm**: RandomForest Classifier
- **Training Accuracy**: 100% (R² = 0.991)
- **Validation Accuracy**: 88.5% (R² = 0.885)
- **Optimal Threshold**: 78.27
- **AUC**: 1.000 (perfect classification on small dataset)

### Risk Stratification Results
- **Low Risk Patients**: 79.2% (Better prognosis, limited immunotherapy response)
- **High Risk Patients**: 20.8% (Higher immune escape risk, better immunotherapy candidates)

### Gene Correlation Insights
- **PDCD1 ↔ CD8A**: r = 0.71 (Strong positive correlation)
- **CD8A ↔ IFNG**: r = 0.69 (Immune activation signature)
- **PDCD1 ↔ IFNG**: r = 0.51 (Moderate correlation)

##  Clinical Applications

###  Low Expression Prediction (Low Immune Escape Risk)
- **Clinical Implication**: Limited response to PD-1/PD-L1 inhibitors
- **Treatment Strategy**: Consider alternative therapies or combination approaches
- **Monitoring**: Standard follow-up protocols

###  High Expression Prediction (High Immune Escape Risk)
- **Clinical Implication**: Enhanced response to immune checkpoint inhibitors
- **Treatment Strategy**: Priority candidates for PD-1/PD-L1 targeted therapy
- **Monitoring**: Close surveillance for immune-related adverse events

## 📁 Repository Structure

```
├── data/                          # Raw and processed datasets
├── notebooks/                     # Jupyter notebooks for analysis
│   ├── data_exploration.ipynb     # Exploratory data analysis
│   ├── model_training.ipynb       # ML model development
├── results/                       # Generated figures and outputs
│   ├── figures/                   # All visualization outputs
│   └── figure.md                  # Detailed figure documentation
│   └── reference.md  
└── README.md                     # This file
```

## 📈 Model Comparison Results

| Algorithm | Training R² | Validation R² | Overfitting Risk |
|-----------|-------------|---------------|------------------|
| **RandomForest** | **0.991** | **0.885** | **Low** |
| Ridge Regression | 0.95 | 0.82 | Low |
| LASSO | 0.93 | 0.79 | Low |
| Linear Regression | 0.89 | 0.75 | Moderate |
| CNN | 1.00 | <0 | **High** |

##  Scientific Impact

### Biological Insights
- **Immune Balance**: Strong correlation between PD-1 and CD8+ T-cell markers suggests coordinated immune regulation
- **Pathway Activation**: Multi-gene signature captures comprehensive immune checkpoint status
- **Therapeutic Target**: Quantifies immune suppression for precision medicine applications

### Clinical Translation
- **Patient Stratification**: Identifies optimal immunotherapy candidates
- **Treatment Optimization**: Reduces ineffective treatment exposure
- **Resource Allocation**: Improves healthcare cost-effectiveness
- **Biomarker Development**: Advances companion diagnostic capabilities

##  Important Limitations

### Statistical Considerations
- **Small Sample Size**: n=24 patients (proof-of-concept study)
- **Perfect Accuracy**: Likely due to limited data, requires larger validation
- **Single Cancer Type**: Breast cancer-specific findings
- **Cross-validation**: Internal validation only, needs external datasets

### Clinical Validation Requirements
- **Regulatory Approval**: Not approved for clinical use
- **Larger Studies**: Multi-center validation needed
- **Prospective Trials**: Real-world outcome validation required
- **Safety Assessment**: Long-term follow-up studies necessary


## References & Future Work

### Potential Extensions
1. **Multi-cancer Validation**: Extend to lung, melanoma, and other cancer types
2. **Combination Biomarkers**: Integrate with tumor mutational burden and microsatellite instability
3. **Longitudinal Analysis**: Track expression changes during treatment
4. **Real-world Evidence**: Collaborate with clinical centers for outcome validation

### Technical Improvements
- Deep learning architectures for larger datasets
- Ensemble methods combining multiple algorithms
- Feature selection optimization
- Automated hyperparameter tuning


* **Disclaimer**: This research tool is designed for scientific investigation only. It has not been validated for clinical diagnostic use and should not influence patient treatment decisions without proper clinical validation and regulatory approval.
