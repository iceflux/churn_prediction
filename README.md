English | [Русский](README.ru.md)

# churn_prediction

![Python](https://img.shields.io/badge/python-3.x-blue)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/z123p2/churn_prediction/blob/main/churn_prediction.ipynb)
![XGBoost](https://img.shields.io/badge/model-XGBoost-orange)
![License](https://img.shields.io/badge/license-MIT-green)

Customer churn prediction model for a telecom operator.
**Algorithm:** XGBoost. **Accuracy:** 79.6%.

## Key results

### 1. Class distribution

![Class distribution](https://github.com/z123p2/churn_prediction/blob/main/images/class_distribution.png?raw=true)

### 2. Feature importance

![Feature importance](https://github.com/z123p2/churn_prediction/blob/main/images/feature_importance.png?raw=true)

### 3. Effect on churn (+ increases, - decreases)

![Feature influence](https://github.com/z123p2/churn_prediction/blob/main/images/churn_influence.png?raw=true)

## Conclusions

**1. Model quality**
- Accuracy: 79.60%
- The model predicts staying customers well (89%), but detects churners worse (54%)

**2. Most important features (what drives churn)**

**Protect against churn (green on the chart):**
- tenure - the longer a customer stays with the company, the less likely they leave
- Contract One year (Contract Two year) - 1 and 2 year contracts strongly reduce churn
- InternetService_No - customers without internet churn less
- TechSupport - tech support helps retain customers

**Increase churn (red on the chart):**
- PaymentMethod Electronic check - electronic checks lead to churn
- InternetService Fiber optic - fiber optic leads to high churn
- PaperlessBilling - paperless billing increases churn
- OnlineSecurity - customers with online security churn more often

**3. What the business should do**
- Move monthly-contract customers to 1-2 year contracts
- Review the quality or price of fiber optic internet compared to competitors
- Retain new customers during the first 3-6 months
- Review the electronic check and paperless billing policies

## How to run

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Open the [notebook](churn_prediction.ipynb) in Colab or Jupyter
3. Run all cells (data is downloaded automatically)

## Technologies

- Python, pandas, numpy
- XGBoost
- scikit-learn
- matplotlib, plotly
