![Project Banner](Used_Car_Price_Banner.png)
# Used Car Price Prediction: Gradient Boosting Model Comparison

**A production ML system design study comparing gradient boosting algorithms for real-time vehicle valuation**

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/Status-Portfolio%20Project-green.svg)]()

---

## 🎯 Project Overview

Rusty Bargain, a used car sales service, required a production-ready machine learning system for their customer-facing mobile app. The challenge: balance three competing business requirements—**prediction accuracy**, **real-time inference speed**, and **training efficiency**—while working under computational constraints.

This project systematically evaluates five algorithms across the accuracy-speed-efficiency spectrum to identify the optimal model for production deployment.

### Key Finding
**LightGBM selected for production:** RMSE of $1,668 with 0.09-second inference time and 43x faster training than Random Forest, making it ideal for systems requiring frequent model updates.

---

## 💼 Business Context

The app provides instant car valuations to potential sellers during active engagement sessions. This creates three critical requirements:

1. **Prediction Quality** - Accurate enough to build customer trust and support pricing decisions
2. **Inference Speed** - Sub-second response time to maintain user engagement  
3. **Training Efficiency** - Fast retraining capability as new inventory data becomes available

These competing demands require strategic model selection beyond pure accuracy optimization.

---

## 🔬 Technical Approach

### Models Evaluated

| Algorithm | Purpose | Key Characteristic |
|-----------|---------|-------------------|
| **Linear Regression** | Baseline | Interpretable, fast inference |
| **Decision Tree** | Non-linear baseline | Feature importance visibility |
| **Random Forest** | Ensemble stability | Best accuracy, slow training |
| **LightGBM** | Speed-optimized boosting | **Production recommendation** |
| **CatBoost** | Native categorical handling | Robust to hyperparameter tuning |
| **XGBoost** | Industry standard | Balanced performance |

### Methodology

- **Dataset:** 354,369 used car listings with technical specifications, condition indicators, and pricing history
- **Evaluation Metric:** RMSE (Root Mean Squared Error) on held-out validation set
- **Performance Tracking:** Training time, prediction time, and accuracy measured for all models
- **Resource Optimization:** Hyperparameter grid reduction to prevent memory constraints while maintaining methodological rigor

---

## 📊 Results Summary

### Model Performance

| Model | RMSE ($) | Training Time (s) | Prediction Time (s) |
|-------|----------|-------------------|---------------------|
| Linear Regression | 2,693 | 0.40 | 0.01 |
| Decision Tree | 2,256 | 34.79 | 0.01 |
| Random Forest | **1,568** | 217.09 | 0.24 |
| **LightGBM** | **1,691** | **5.05** | **0.09** |
| CatBoost | 1,776 | 87.24 | 0.04 |
| XGBoost | 1,643 | 223.19 | 0.15 |

### Strategic Recommendation

**LightGBM** provides the optimal balance:
- Competitive accuracy (RMSE: $1,691 vs best of $1,568)
- **43x faster training** than Random Forest (5.05s vs 217.09s)
- Sub-second inference for real-time user experience
- Efficient memory utilization for deployment at scale

While Random Forest achieved the lowest RMSE, LightGBM's dramatic training speed advantage makes it superior for production systems requiring frequent model updates with new inventory data.

---

## 🛠️ Technical Skills Demonstrated

### Machine Learning
- Gradient boosting algorithms (LightGBM, XGBoost, CatBoost)
- Ensemble methods (Random Forest)
- Hyperparameter tuning and model selection
- Train/validation/test split methodology

### Production ML Considerations
- Multi-objective optimization (accuracy vs speed vs efficiency)
- Resource-constrained model development
- Performance profiling and benchmarking
- Strategic tradeoff analysis for deployment decisions

### Data Engineering
- Handling high-cardinality categorical features
- Feature encoding strategies
- Large dataset processing (350K+ records)
- Memory optimization techniques

---

## 📁 Project Structure

```
used-car-pricing-gradient-boosting/
│
├── Project12_UsedCarPricing_Portfolio.ipynb    # Complete analysis notebook
└── README.md                                    # This file
```

---

## 🚀 How to Use This Repository

### View the Analysis
Click on `Project12_UsedCarPricing_Portfolio.ipynb` above to see the full analysis rendered directly in GitHub.

### Run Locally
```bash
# Clone the repository
git clone https://github.com/drdanishalthomas/used-car-pricing-gradient-boosting.git

# Navigate to directory
cd used-car-pricing-gradient-boosting

# Install dependencies
pip install pandas numpy scikit-learn lightgbm xgboost catboost matplotlib seaborn

# Launch Jupyter
jupyter notebook Project12_UsedCarPricing_Portfolio.ipynb
```

---

## 💡 Key Insights for Production ML

### 1. **The Best Model ≠ The Best Solution**
Random Forest had the lowest RMSE but wasn't optimal for production due to prohibitive training time for systems requiring frequent updates.

### 2. **Resource Constraints Drive Design**
Working under memory limitations required strategic hyperparameter grid reduction—demonstrating that effective ML isn't just about unlimited compute.

### 3. **Business Requirements Define Success**
The three-way tradeoff between accuracy, speed, and training time mirrors real-world production constraints where technical excellence must align with operational feasibility.

---

## 📫 Connect

**Danisha L. Thomas, PhD**  
Clinical Psychologist | Data Scientist | Behavioral Intelligence Specialist

- 🔗 [LinkedIn](https://www.linkedin.com/in/drdanishalthomas)
- 💼 [GitHub Portfolio](https://github.com/drdanishalthomas)

---

## 📝 Project Context

This analysis demonstrates systematic model evaluation for production deployment, balancing competing business requirements under resource constraints—core competencies for behavioral intelligence and data science roles in government and defense contracting.

**Skills:** Python • Gradient Boosting • LightGBM • XGBoost • CatBoost • Production ML • Resource Optimization • Strategic Decision-Making

---

*This project showcases production ML system design with emphasis on strategic model selection and operational constraints—essential capabilities for deploying AI systems in resource-limited environments.*
