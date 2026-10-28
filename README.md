# UK Birth Rate Forecasting Using Deep Learning

### A Comparative Study of LSTM, GRU and CNN Models

## Project Overview

This project explores how deep learning can be used to forecast birth rate trends in the United Kingdom.

Historical birth rate data from 1960 to 2023 is analysed to understand long-term changes and develop forecasting models.

Three deep learning models, Long Short-Term Memory (LSTM), Gated Recurrent Unit (GRU) and Convolutional Neural Network (CNN), are developed and compared to evaluate their ability to predict future birth rates.

The project also generates birth rate forecasts up to 2030 using a GRU ensemble model.

## Project Objectives

- Analyse historical UK birth rate trends.
- Identify patterns and relationships in time-series data.
- Develop LSTM, GRU and CNN forecasting models.
- Compare model performance using regression evaluation metrics.
- Forecast future birth rates up to 2030.

## Dataset

The project uses historical annual crude birth rate data for the United Kingdom.

**Dataset details:**

- Country: United Kingdom
- Period: 1960–2023
- Data type: Annual time series
- Target variable: Crude birth rate
- Unit: Births per 1,000 people
- Input file: `birthrates.csv`

The dataset contains annual observations used for model training, testing and forecasting.

## Technologies Used

**Programming language:** Python

**Development environment:** Jupyter Notebook / Google Colab

**Libraries:**
- Pandas and NumPy – Data processing
- Matplotlib and Seaborn – Data visualisation
- TensorFlow and Keras – Deep learning
- Scikit-learn – Data scaling and model evaluation
- Statsmodels – Time-series analysis utilities

## Project Methodology

### 1. Data Preparation

- Load the historical birth rate dataset.
- Filter the records for the United Kingdom.
- Prepare annual birth rate observations for time-series analysis.
- Apply differencing and Min-Max scaling for model training.

### 2. Exploratory Data Analysis

Explore historical birth rate patterns through:

- Historical trend analysis
- Distribution plots
- Box plots
- Lag plots
- Autocorrelation analysis

### 3. Model Development

**LSTM (Long Short-Term Memory)**

A recurrent neural network designed to learn patterns and dependencies in sequential data.

**GRU (Gated Recurrent Unit)**

A recurrent neural network that uses gating mechanisms to model time-series relationships.

**CNN (Convolutional Neural Network)**

A neural network that uses convolutional layers to identify local patterns within historical observations.

Each model is trained using an ensemble approach with five model instances.

### 4. Training and Testing

The dataset is divided chronologically:

- Training period: 1960–2010
- Testing period: 2011–2023
- Input lookback window: 5 observations

Early stopping is used during model training to limit unnecessary training and help reduce overfitting.

### 5. Model Evaluation

Model performance is measured using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score
- Mean Absolute Percentage Error (MAPE)

The models are compared using their predictions on the test dataset.

## Future Birth Rate Forecasting

The project uses the GRU ensemble model to generate forecasts for 2024–2030.

A recursive forecasting approach is used, where predicted changes are used to estimate subsequent annual birth rates.

These forecasts are model estimates based on historical trends and should not be treated as official population projections.

## Project Visualisations

The notebook includes:

- Historical UK birth rate trends
- Birth rate distribution and autocorrelation
- Training and validation loss curves
- Actual versus predicted birth rates
- Model performance comparison
- Forecast birth rate trends to 2030

## How to Run the Project

1. Download or clone the repository.
2. Open `finalversion2.ipynb` in Jupyter Notebook or Google Colab.
3. Install the required Python libraries.
4. Add the `birthrates.csv` dataset to the working directory.
5. Run the notebook cells in order.
6. Review the evaluation metrics, prediction plots and forecasts.

**Note:** The notebook requires the historical data file and a defined birth rate time series before execution.

## Limitations and Future Improvements

The study uses annual historical data for a single country, which limits the amount of training data available for deep learning.

Future improvements could include:

- Comparing against simple statistical forecasting baselines.
- Using rolling or walk-forward validation.
- Including economic and demographic indicators.
- Comparing forecasts across different countries.
- Improving model tuning and forecast uncertainty estimates.

## Conclusion

This project demonstrates the application of deep learning techniques to demographic time-series forecasting.

By developing and comparing LSTM, GRU and CNN models, the project provides a framework for analysing historical birth rate patterns, evaluating forecasting methods and exploring future trends in the United Kingdom.

The work highlights how Python and deep learning can support data-driven demographic analysis.
