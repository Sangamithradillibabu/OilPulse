OilPulse:

This project analyzes Brent oil daily prices as a time series to detect unusual patterns, spikes, and potential crisis events. Since oil prices are sequential and influenced by past trends, time series analysis is essential to identify anomalies effectively.



How It Works:
Data Preprocessing
Historical Brent oil prices are loaded and sorted by date.
Additional features are created:
lag_7 → price 7 days ago
rolling_mean_7 → 7-day moving average
rolling_std_7 → 7-day standard deviation



Train-Test Split:
The first 60% of the data is used for training, and the remaining 40% for testing.


Anomaly Detection Methods:
ARIMA: Predicts expected prices and flags deviations as anomalies.

Isolation Forest: Detects unusual points considering multiple features simultaneously.

CUSUM: Tracks cumulative changes to highlight sudden shifts in price trends.


Scoring and Event Classification:
Anomalies from all three methods are combined into a score for each day.
Each day is classified as:
Normal → no anomalies
Weak → 1 anomaly detected
Warning → 2 anomalies detected
Crisis → all 3 anomalies detected


Visualization:
Price chart shows anomalies with color-coded markers:
Green = CUSUM
Orange = Isolation Forest
Red = ARIMA
Purple star = Crisis events

Historical crises like COVID-19 Crash and Arab Spring are annotated.
Shaded regions highlight known crisis periods for better context.



Why This Project is Useful:
Provides an early warning system for sudden oil price changes.
Combines statistical modeling and machine learning for robust detection.
Helps understand how real-world events impact commodity prices.
Visual outputs make it easy to spot significant anomalies and crises.



Key Results:
Total data points: 3942
ARIMA anomalies: 185
CUSUM anomalies: 3940
Isolation Forest anomalies: 1063
Crisis events detected: 103



How to Run:

1.Open the notebook (oil_anomaly.ipynb) in Colab or Jupyter Notebook.
2.Run all cells sequentially — it loads data, generates predictions, detects anomalies, and plots results.
3.Optional: ARIMA predictions are cached in arima_predictions.csv to save time.



