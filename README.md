# Car Sales Prediction with ML.NET

This repository contains a machine learning project that predicts car sales in Brazil using ML.NET and AutoML. The project includes data preprocessing, model training, evaluation, and visualization of historical sales data alongside future predictions.

## Project Structure

```
/
├── bcdata.sgs.1378.csv           # Historical car sales data (1981-2025)
├── automl-predictive-cars-sales.ipynb  # Jupyter notebook for model training
├── use-existing-model.ipynb      # Jupyter notebook for predictions and visualization
├── graph.html                    # Interactive visualization of results
└── model.mlnet                   # Serialized ML model (generated after training)
```

## Key Features

- **AutoML Integration**: Uses ML.NET's AutoML to automatically find the best regression model
- **Time Series Prediction**: Forecasts car sales for the next 12 months
- **Interactive Visualization**: Plotly-powered chart showing historical data and predictions
- **High Accuracy**: Achieves R² score of 0.908 on test data

## How It Works

1. **Data Preparation**:
   - Loads historical car sales data from CSV
   - Extracts year and month features from dates
   - Normalizes features for better model performance

2. **Model Training**:
   - Uses AutoML to evaluate different algorithms
   - Optimizes for R² (coefficient of determination)
   - Saves the best performing model to `model.mlnet`

3. **Prediction**:
   - Loads the trained model
   - Generates forecasts for the next 12 months
   - Visualizes historical data alongside predictions

## Results

The best model achieved:
- **R²**: 0.908
- **MAE**: 17,980.202
- **RMSE**: 23,414.955

![Prediction Visualization](graph.html)

## Requirements

- .NET 6.0+
- ML.NET packages:
  - Microsoft.ML.AutoML
  - Microsoft.Data.Analysis
- Plotly.NET (for visualization)

## Usage

1. Run `automl-predictive-cars-sales.ipynb` to train and save the model
2. Run `use-existing-model.ipynb` to generate predictions and visualizations
3. Open `graph.html` to view the interactive chart

## Future Improvements

- Incorporate additional economic indicators
- Implement more sophisticated time series modeling
- Add hyperparameter tuning beyond AutoML defaults
- Create a web API for real-time predictions

## Data Source

Historical car sales data provided by the Brazilian Central Bank (BCB) - Series 1378.
