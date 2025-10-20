# 📊 Figure Documentation: PDCD1 Expression Prediction System

## Project Overview
This documentation presents a comprehensive analysis workflow and results of a PDCD1 expression prediction system based on PD-1/PD-L1 immune checkpoint pathway-related genes.

---

## 🔍 Figure 1: Comprehensive Tumor Immune Escape Data Analysis
![Comprehensive Analysis](https://github.com/jaywang-cpu/-BDS-final-breast-cancer-immune-escape-gnn/blob/main/results/Comprehensive%20Tumor%20Immune%20Escape%20Data%20Analysis.png)

### Analysis Objective
Conduct comprehensive exploratory analysis of immune-related gene expression data in breast cancer patients to provide a data foundation for subsequent modeling.

### Key Findings
- **PDCD1 Expression Distribution**: Most patients show low expression levels, with 80th percentile at 133.0
- **Risk Stratification**: 79.2% low-risk patients vs. 20.8% high-risk patients
- **Gene Correlation**: Strong positive correlation between PDCD1 and CD8A (r=0.71), indicating immune activation-suppression balance
- **Expression Heterogeneity**: Significant inter-patient variability in immune gene expression patterns

### Biological Implications
The correlation matrix reveals coordinated immune gene expression, supporting the rationale for multi-gene predictive modeling in immune checkpoint therapy selection.

---

## 🧬 Figure 2: Immune Checkpoint Gene Expression Prediction Tool
![Prediction Interface](https://raw.githubusercontent.com/jaywang-cpu/-BDS-final-breast-cancer-immune-escape-gnn/main/results/Immune%20Checkpoint%20Gene%20Expression%20Predictor.jpg)

### System Functionality
Interactive machine learning-based PDCD1 expression prediction system integrating 5 key immune genes for comprehensive assessment.

### Technical Specifications
- **Gene Weights**: CD274(43.9%) > CD8A(23.9%) > PRF1(10.5%) > IFNG(8.4%) > GZMB(7.9%)
- **Training Dataset**: 24 samples with 2:1 training/testing ratio
- **Algorithm**: RandomForest-based ensemble method
- **Safety Protocol**: Clearly labeled for research use only, not for clinical decision-making

### Clinical Integration
The user-friendly interface allows real-time prediction with confidence intervals and treatment recommendations based on expression profiles.

---

## 📈 Figure 3: Machine Learning Model Performance Evaluation Report
![Model Performance](https://raw.githubusercontent.com/jaywang-cpu/-BDS-final-breast-cancer-immune-escape-gnn/main/results/Machine%20Learning%20Model%20Performance%20Evaluation%20Report.png)

### Model Validation Results
Comprehensive evaluation of RandomForest baseline model classification performance across 9 key assessment metrics.

### Performance Highlights
- **Perfect Classification**: All RandomForest variants achieve AUC=1.000
- **Feature Importance**: TMI1 gene contributes most significantly (0.369), followed by CD8A (0.305)
- **Learning Curves**: Training and validation AUC remain stable at 1.0 (*Note: Due to limited dataset size*)
- **Threshold Optimization**: Optimal threshold at 0.760 balancing sensitivity and specificity
- **Cross-Validation**: Model demonstrates stability across different data splits
- **Precision-Recall**: Perfect precision-recall performance indicating robust classification

### Model Limitations
The perfect accuracy metrics likely reflect the small sample size (n=24) and should be validated on larger, independent datasets.

---

## ⚖️ Figure 4: Multi-Algorithm Model Performance Comparison Analysis
![Model Comparison](https://raw.githubusercontent.com/jaywang-cpu/-BDS-final-breast-cancer-immune-escape-gnn/main/results/Multi-Algorithm%20Model%20Performance%20Comparison.png)

### Algorithm Benchmarking
Systematic comparison of 7 machine learning algorithms for PDCD1 expression prediction performance.

### Key Conclusions
- **Best Model**: RandomForest demonstrates superior performance on both training and validation sets
- **Overfitting Analysis**: CNN model shows severe overfitting (Training R²=1.0, Validation R²<0)
- **Model Robustness**: Traditional ML methods (RF, Ridge, LASSO) exhibit greater stability
- **Prediction Accuracy**: RandomForest achieves Training R²=0.991, Validation R²=0.885
- **Generalization**: Linear models show better generalization despite lower training performance

### Algorithm Selection Rationale
RandomForest's ensemble approach provides optimal balance between accuracy and generalizability for this immune gene expression task.

---

## 🟢 Figure 5: Low Immune Suppression Risk Patient Prediction
![Low Risk Prediction](https://raw.githubusercontent.com/jaywang-cpu/-BDS-final-breast-cancer-immune-escape-gnn/main/results/Low%20Immune%20Suppression%20Risk%20Patient.png)

### Prediction Output
Model prediction results for a specific patient sample showing low PDCD1 expression and associated clinical implications.

### Clinical Interpretation
- **Prediction Probability**: 73.8% probability of low expression
- **Risk Score**: 42.21 (below threshold of 78.27)
- **Treatment Recommendation**: Limited response expected to PD-1/PD-L1 inhibitor therapy
- **Model Confidence**: 73.8% confidence level
- **Alternative Strategies**: Consider combination therapies or alternative immunotherapeutic approaches

### Personalized Medicine Impact
This prediction enables clinicians to optimize treatment selection and avoid ineffective therapies in low-expression patients.

---

## 🔴 Figure 6: High Immune Suppression Risk Patient Prediction
![High Risk Prediction](https://raw.githubusercontent.com/jaywang-cpu/-BDS-final-breast-cancer-immune-escape-gnn/main/results/High%20Immune%20Suppression%20Risk%20Patient.png)

### Prediction Output
Model prediction for high PDCD1 expression patient with personalized treatment guidance.

### Clinical Value
- **Prediction Probability**: 71.4% probability of high expression
- **Risk Score**: 107.99 (exceeds threshold of 78.27)
- **Treatment Advantage**: Enhanced response likelihood to immune checkpoint inhibitor therapy
- **Precision Medicine**: Scientific basis for immunotherapy patient selection
- **Monitoring Strategy**: Recommend close monitoring for immune-related adverse events

### Therapeutic Implications
High-expression patients represent optimal candidates for PD-1/PD-L1 targeted therapies with improved response rates.

---

## 🎯 System Overall Value

### Clinical Application Prospects
1. **Patient Stratification**: Identify immunotherapy-advantaged populations
2. **Treatment Decision Support**: Assist in personalized treatment planning
3. **Prognostic Assessment**: Predict immune escape risk profiles
4. **Resource Optimization**: Improve therapeutic resource allocation efficiency
5. **Biomarker Development**: Advance companion diagnostic capabilities

### Technical Innovation Points
- **Multi-gene Integration**: Comprehensive pathway-based prediction model
- **Real-time Interface**: Interactive prediction with immediate clinical guidance
- **Comprehensive Validation**: Robust model evaluation framework
- **Clinical Translation**: Clear therapeutic application guidelines
- **Scalable Architecture**: Expandable to additional cancer types and biomarkers

### Future Directions
- Validation on larger, multi-center datasets
- Integration with additional immune markers
- Development of combination therapy prediction models
- Real-world clinical outcome validation

---

## 📊 Statistical Summary

| Metric | Value | Clinical Significance |
|--------|-------|----------------------|
| Sample Size | 24 patients | Proof-of-concept study |
| Model Accuracy | 100% (small dataset) | Requires larger validation |
| Prediction Threshold | 78.27 | Optimized for clinical utility |
| Gene Panel Size | 5 genes | Focused immune pathway analysis |
| Cross-validation Stability | High | Robust model performance |

---

*⚠️ **Important Disclaimer**: This system is developed based on a small dataset (n=24) and is intended for research use only. It should NOT be used for clinical diagnostic decision-making without proper validation on larger, independent patient cohorts. Clinical implementation requires regulatory approval and extensive validation studies.*

*🔬 **Research Ethics**: All analyses comply with institutional review board guidelines and patient privacy regulations.*
