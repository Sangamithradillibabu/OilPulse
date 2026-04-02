Oil Price Anomaly Detection Project
Overview:

This project analyzes Brent oil daily prices and automatically detects unusual price movements using three methods:

ARIMA – detects deviations from predicted price trends
Isolation Forest – identifies unusual points in the data
CUSUM – tracks cumulative shifts in price

The anomalies from all three methods are combined into a score to classify each day as:

Normal- Weak -Warning -Crisis 

It also visualizes historical crises like COVID-19, Arab Spring, and geopolitical events alongside current anomalies.

Key Features:

1.Automatic detection of anomalies and crises
2.Combines statistical, ML, and cumulative detection methods
3.Visualizations with clear markers and annotations
4.Event scoring for risk assessment

What You’ll See
Price chart with colored markers:

Green = CUSUM anomalies
Orange = Isolation Forest anomalies
Red = ARIMA anomalies
Purple star = Crisis events
Historical crisis periods shaded on the timeline
Annotated important events

Highlights from the Analysis:

Total data points: 3942
ARIMA detections: 185
CUSUM detections: 3940
Isolation Forest detections: 1063
Crisis events detected: 103

How to Run:
1.Open the notebook (oil_anomaly.ipynb) in Colab or Jupyter Notebook.
2.Run all cells sequentially — it loads data, generates predictions, detects anomalies, and plots results.
3.Optional: ARIMA predictions are cached in arima_predictions.csv to save time.



