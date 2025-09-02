# 🌍 Global Temperature Prediction using Random Forest

This project analyzes and predicts **global land and ocean temperatures** using historical climate data.  
The dataset is preprocessed, converted from Celsius to Fahrenheit, and modeled using a **Random Forest Regressor** to estimate temperature trends.

---

## 📂 Project Structure

- GlobalTemperatures.csv # Dataset (from Kaggle)
- temperature_prediction.ipynb # Jupyter Notebook with full code
- README.md # Project documentation


---

## 📊 Dataset

- Source: [Kaggle - Global Land and Ocean Temperatures](https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data)
- Columns used:
  - `LandAverageTemperature`
  - `LandMaxTemperature`
  - `LandMinTemperature`
  - `LandAndOceanAverageTemperature` (Target)
  - `dt` (date)

The dataset spans from **1750 onwards**, but we focus on **1850+** for data quality.

---

## ⚙️ Workflow

1. **Data Wrangling**
   - Converted temperatures from Celsius → Fahrenheit
   - Extracted year from `dt` column
   - Removed unnecessary uncertainty columns
   - Filtered data from 1850 onwards

2. **Exploratory Data Analysis (EDA)**
   - Correlation heatmap of temperature features
   - Time-series exploration of global temperature rise

3. **Modeling**
   - Features: `LandAverageTemperature`, `LandMaxTemperature`, `LandMinTemperature`
   - Target: `LandAndOceanAverageTemperature`
   - Train-test split (75%-25%)
   - Random Forest Regressor with scaling & feature selection

4. **Evaluation Metrics**
   - **Baseline MAE** (using mean predictor)
   - **Random Forest MAE, RMSE, Accuracy**

---

## 📈 Results

- **Baseline MAE:** ~ (value depends on dataset split)
- **Random Forest MAE:** Much lower than baseline
- **Accuracy (MAPE-based):** ~90%+

The model shows strong predictive performance for global temperature estimation.

---

## 🔮 Visualizations

- Correlation Heatmap between temperature features
- Actual vs Predicted Land & Ocean Average Temperature (line chart)

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/global-temp-prediction.git
   cd global-temp-prediction
   ```

2. Install Dependencies
    pip install -r requirements.txt



## Screenshots
<img width="1060" height="880" alt="image" src="https://github.com/user-attachments/assets/cf358e9c-2032-4a4b-b832-82dd243d551d" />
<img width="597" height="381" alt="image" src="https://github.com/user-attachments/assets/b93e1d7c-35e8-46ad-92ba-5da102370328" />

