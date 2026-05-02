# CKD Prediction Research - Presentation Materials

## Overview

This folder contains complete presentation materials for the research paper:

**"A Comparative Study, Prediction and Development of Chronic Kidney Disease Using Machine Learning on Patients Clinical Records"**  
Hassan et al. (2023), *Human-Centric Intelligent Systems*, 3:92–104  
DOI: https://doi.org/10.1007/s44230-023-00017-3

## Key Results

✅ **100% Accuracy** - SVM with XGBoost-selected features  
✅ **All models >96%** accuracy  
✅ **72% feature reduction** (25 → 7 features)  
✅ **Clinically interpretable** (SHAP-based explanations)  
✅ **Competitive with state-of-the-art** literature

## Presentation Files

### Main Presentation Files

1. **CKD_Prediction_Presentation.pptx**
   - PowerPoint presentation (40 slides)
   - Ready to present
   - Professional formatting

2. **presentation.html**
   - Interactive web-based presentation
   - Navigate with arrow keys
   - View in any browser

3. **presentation_slides.md**
   - Markdown source for all slides
   - Easy to edit and customize
   - Can regenerate PPTX/HTML

### Speaker Support

4. **SPEAKER_NOTES.md**
   - Detailed notes for all 40 slides
   - Timing suggestions (~45-50 min)
   - Key talking points
   - Anticipated Q&A
   - Presenter tips

5. **PRESENTATION_SUMMARY.txt**
   - Quick reference guide
   - File descriptions
   - Usage instructions
   - Performance summary

### Generation Script

6. **generate_presentation.py**
   - Regenerate presentations from markdown
   - Customize formatting
   - Create updated versions

## Presentation Structure (40 Slides)

### Part 1: Introduction (Slides 1-4)
- Title and abstract
- Problem statement
- Literature review

### Part 2: Methodology (Slides 5-11)
- Data description
- Preprocessing (PMM imputation)
- K-means clustering (k=3)
- XGBoost feature selection
- Dataset splitting (80/20)

### Part 3: Analysis (Slides 12-16)
- 5 ML models (NN, RF, SVM, RT, BTM)
- Performance metrics
- Results comparison
- Confusion matrices

### Part 4: Results (Slides 17-21)
- Literature comparison
- Key findings
- Visualizations
- SHAP analysis

### Part 5: Conclusions (Slides 22-33)
- Clinical relevance
- Implementation roadmap
- Ethical considerations
- Cost-benefit analysis
- Future directions
- Q&A

### Part 6: Appendix (Slides 34-40)
- Technical specifications
- Code structure
- Data quality
- Deployment architecture
- References

## Research Visualizations

All figures from the paper are available:

| File | Description | Paper Figure |
|------|-------------|--------------|
| `missing_data_plot.png` | Missing value analysis | Fig. 2 |
| `clustering_analysis.png` | K-means & dendrogram | Fig. 3 |
| `shap_summary.png` | Feature importance | Fig. 4 |
| `shap_scatter.png` | Feature impact | Fig. 5 |
| `model_comparison.png` | Performance comparison | Figs. 6-9 |
| `confusion_matrices.png` | All model confusion matrices | - |

## Model Performance Summary

| Model | Dataset | Accuracy | Sensitivity | Specificity | Kappa |
|-------|---------|----------|-------------|-------------|-------|
| **SVM** | **XGBoost** | **100.00%** | **100.00%** | **100.00%** | **100.00%** |
| SVM | Full | 98.75% | 97.50% | 100.00% | 97.50% |
| RF | XGBoost | 98.75% | 97.50% | 100.00% | 97.50% |
| RF | Full | 98.75% | 97.50% | 100.00% | 97.50% |
| NN | XGBoost | 97.50% | 95.00% | 100.00% | 95.00% |
| NN | Full | 97.50% | 95.00% | 100.00% | 95.00% |
| RT | XGBoost | 96.25% | 95.00% | 97.50% | 92.50% |
| RT | Full | 96.25% | 95.00% | 97.50% | 92.50% |
| BTM | XGBoost | 97.50% | 95.00% | 100.00% | 95.00% |
| BTM | Full | 96.25% | 95.00% | 97.50% | 92.50% |

## Top 7 Features (XGBoost Selection)

1. **Hemoglobin (hemo)** - Anemia indicator in CKD
2. **Serum Creatinine (sc)** - Kidney filtration marker
3. **Packed Cell Volume (pcv)** - Red blood cell concentration
4. **Albumin (al)** - Protein leakage indicator
5. **Pedal Edema (pe)** - Fluid retention sign
6. **Blood Pressure (bp)** - Hypertension comorbidity
7. **Specific Gravity (sg)** - Urine concentration ability

All features are established CKD markers in clinical practice!

## How to Use

### For Presentation

```bash
# Option 1: PowerPoint (recommended)
Open CKD_Prediction_Presentation.pptx
Review SPEAKER_NOTES.md
Present!

# Option 2: Web Browser
Open presentation.html in Chrome/Firefox/Safari
Navigate with arrow keys
Present!
```

### For Customization

```bash
# Edit the markdown slides
nano presentation_slides.md

# Regenerate presentations
python generate_presentation.py

# New files will be created:
# - CKD_Prediction_Presentation.pptx
# - presentation.html
```

### For Printing Handouts

```bash
# From PowerPoint:
File → Export → Create PDF
Print as handout (6 slides per page)

# Or use presentation.html:
Print → Save as PDF
```

## Code Reference

The actual implementation is in `code.ipynb`:

- **Cell 1-4**: Data loading & exploration
- **Cell 5-7**: Preprocessing & imputation
- **Cell 8**: K-means clustering
- **Cell 9-11**: XGBoost feature selection
- **Cell 10-12**: SHAP analysis
- **Cell 13**: Dataset splitting
- **Cell 14-19**: Model training
- **Cell 20-24**: Results & visualization

## Comparison with Literature

| Study | Accuracy | Method |
|-------|----------|--------|
| **Our Work (SVM+XGBoost)** | **100.00%** | **SVM + Feature Selection** |
| Our Work (RF) | 98.75% | Random Forest |
| Almansour et al. [26] | 99.75% | Neural Network |
| Hore et al. [28] | 92.54% | Random Forest |
| Khan et al. [12] | 98.25% | SVM |
| Almustafa et al. [32] | 95.50% | Random Tree |
| Hasan et al. [34] | 96.00% | Bagging Tree |

Our results are **competitive with or exceed state-of-the-art**!

## Technical Requirements

### To View Presentations
- PowerPoint (for .pptx)
- Web browser (for .html)
- PDF reader (for printed version)

### To Regenerate
```bash
pip install python-pptx
python generate_presentation.py
```

### To Run Code
```bash
pip install pandas numpy scikit-learn xgboost shap matplotlib seaborn
jupyter notebook code.ipynb
```

## Presentation Tips

⏱ **Timing**: 45-50 minutes + 10 min Q&A  
🎯 **Key Message**: "100% accuracy with interpretable ML"  
📊 **Show**: Visualizations (have them ready)  
📝 **Handouts**: Print key slides  
❓ **Q&A**: Review SPEAKER_NOTES.md  
🎤 **Practice**: Run through at least once  
⏸ **Pause**: Emphasize the 100% result  
🤝 **Engage**: Make it interactive  
📈 **Vision**: Patient impact & future potential  

## Key Messages

1. **Feature Engineering Matters**: 25 → 7 features without losing accuracy
2. **Interpretability is Crucial**: SHAP values provide clinical explanations
3. **Perfect Performance Possible**: 100% accuracy on test set
4. **Clinically Validated**: All features are established biomarkers
5. **Ready for Deployment**: Systematic pipeline, reproducible results

## Clinical Impact

- **Early Detection**: Identify CKD before symptoms appear
- **Cost Savings**: Prevent progression to end-stage renal disease
- **Better Outcomes**: Timely intervention improves survival
- **Accessibility**: Simple test using routine clinical markers

## Future Work

- Multi-hospital validation
- EHR integration
- Regulatory approval (FDA/CE)
- Real-time screening tools
- Multi-language support
- Pediatric adaptation

## References

**Primary Source:**
Hassan, M.M., Hassan, M.H., Mollick, S., et al. (2023). 
"A Comparative Study, Prediction and Development of Chronic Kidney Disease Using Machine Learning on Patients Clinical Records." 
*Human-Centric Intelligent Systems*, 3:92–104. 
https://doi.org/10.1007/s44230-023-00017-3

**Dataset:**
UCI Machine Learning Repository: Chronic Kidney Disease Dataset
https://archive.ics.uci.edu/ml/datasets/Chronic_Kidney_Disease

## Contact

For questions or collaboration:
- See institutional emails in paper
- Research team: Multiple Bangladeshi universities
- VRD Research Lab, Khulna

---

**Last Updated**: May 2, 2026  
**Version**: 1.0  
**Status**: Ready for presentation

⭐ **Good luck with your presentation!** ⭐
