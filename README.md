# **Crop Yield Forecasting**

This repository hosts the complete workflow for forecasting agricultural yield using reservoir metrics like **Level** and **Current Live Storage**, across multiple state–crop pairs in India. The approach integrates time series modeling and machine learning to predict yield from hydrological trends.

---

## **Repository Structure**

```
├── merged_gram_reservoir.csv
├── merged_massor_reservoir.csv
├── merged_mustard_reservoir.csv
├── merged_potato_reservoir.csv
├── merged_rabi_rice_reservoir.csv
├── merged_wheat_reservoir.csv
│
├── yield_analysis_EDA.ipynb
├── yield_analysis_forecast.ipynb
│
├── engineered_state_crop_csvs/
│   └── [Cleaned & feature-engineered data files per state–crop pair]
│
├── filtered_state_crop_csvs/
│   └── [Raw but filtered CSVs by valid state–crop combinations]
│
├── predicted_yield/
│   └── [Forecast outputs per state–crop pair using trained models]
```

---

## **Project Summary**

This project was conducted as part of a summer internship under IDEAS, ISI Kolkata, aiming to forecast crop yields using time series data of reservoir behavior. Key components include:

* **Reservoir Forecasting**: Using Prophet models to predict daily water level and storage for 180 days ahead.
* **Feature Engineering**: Lag and rolling averages for 7-day windows to simulate water stress effects.
* **Modeling**: Random Forest Regression used for yield prediction.
* **Evaluation**: Metrics like R², RMSE, MAE were calculated per crop–state pair.
* **Visualization**: Forecasted vs actual yield plots and rolling trend lines included.

---

## **Notebooks**

| Notebook                        | Purpose                                                                        |
| ------------------------------- | ------------------------------------------------------------------------------ |
| `yield_analysis_EDA.ipynb`      | Exploratory analysis on merged datasets and basic feature inspection.          |
| `yield_analysis_forecast.ipynb` | Full pipeline: reservoir forecasting → feature engineering → yield prediction. |

---

## **Data Folders**

### `engineered_state_crop_csvs/`

* Final daily-resolution CSVs with engineered features (`level_7d_avg`, `level_7d_lag`, etc.).
* Used for training and validating crop-specific models.

### `filtered_state_crop_csvs/`

* Input-level filtered data for valid crop–state pairs (minimum 365 rows & known yields).

### `predicted_yield/`

* Contains future yield forecasts using trained models and Prophet reservoir predictions.
* Includes daily resolution forecast for 180+ days ahead for each pair.

---

## **Technologies Used**

* Python
* Pandas, NumPy, Matplotlib, Seaborn
* Prophet (for time-series forecasting)
* Scikit-learn (for Random Forest Regression)

---

## **Report and Documentation**

This repository is part of a ISI Kolkata IDEAS summer internship project. Detailed project report and appendices (feature importances, yield trends, model metrics) are provided separately in the report submission.

---


## **Contributors**

* [Anmol Gupta](https://www.linkedin.com/in/statisticssensei/)
  
---

