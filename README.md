# Rainfall-Prediction
A machine learning project for 2nd Year Computer Science. Comparing Random Forest and RBF-kernel Support Vector Regression (SVR) for predicting rainfall in three weather stations in Wales: Cardiff, Aberporth and Valley. 

**Note:** Scenario and datasets provided as part of coursework.

Implementation of each model and comparison of the results were done in a Jupyter Notebook. Methodology, findings, and evaluation were summarized in a research poster.

## Project Files

- `Rainfall_Forecasting.ipynb`: Main notebook 
- `Rainfall-Forecasting.pdf`: Project poster
- `cardiff.npy`, `aberporth.npy`, `valley.npy`: Weather station data used for prediction

# Requirements

- Python 3.11
- `numpy`, `pandas`, `matplotlib`, `scikit-learn`

```bash
pip install numpy pandas matplotlib scikit-learn
```

# How to Run

1. Keep the three `.npy` files in the same folder as the notebook
2. Open `Rainfall_Forecasting.ipynb` in Jupyter or Google Colab
3. Run all cells from top to bottom

**Note:** The notebook was written in Google Colab and uses `google.colab.files` to upload the data. If you run it locally, remove that upload cell and load the files directly.

# Summary

## Dataset

Three `.npy` files with 6 columns of information. For the models, only 2 features were used to predict the target.

- **Features:** minimum and maximum temperature
- **Target:** monthly rainfall (mm)

## Method

- **Split:** 80% train / 20% test for both models
- **Preprocessing:** missing values and distribution checked, features standardised for SVR
- **Tuning:** grid search with 5-fold cross-validation on training set
- **Metric:** RMSE, MAE and R²

## Results

**Key findings:**
- SVR beat Random Forest on every metric at all three stations, and was faster to tune
- Temperature alone explains little variation in rainfall (R² of only 0.10-0.35)
- Both models tended to underpredict the wettest months




