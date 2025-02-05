# Fraud Detection Model Performance Monitoring

## Overview
This repository contains code for monitoring the performance of a fraud detection model using **NannyML**. The analysis includes detecting model drift, identifying feature correlation with performance, and tracking key financial metrics.

## Files in Repository
- `reference.csv`: Historical transaction data used for training and baseline comparison.
- `analysis.csv`: New transaction data used for performance evaluation.
- `fraud_detection_analysis.py`: Python script for model performance monitoring and drift detection.
- `README.md`: Documentation and usage guide.

## Key Features
- **Performance Monitoring**: Calculates realized vs. estimated accuracy and detects performance alerts.
- **Feature Drift Analysis**: Uses statistical tests (Kolmogorov-Smirnov, Chi-square) to detect changes in key features.
- **Correlation Ranking**: Identifies which features contribute most to model drift.
- **Transaction Trend Analysis**: Monitors monthly average transaction amounts and detects anomalies.

## Installation
Ensure you have Python 3.x installed. Then install the required dependencies:

```bash
pip install pandas nannyml matplotlib
```

## Usage
Run the `fraud_detection_analysis.py` script:

```bash
python fraud_detection_analysis.py
```

## Results & Insights
### 1. **Model Performance Alerts**
Detected significant drops in performance in **April, May, and June 2019**.

### 2. **Feature Drift Analysis**
- `time_since_login_min` had the highest correlation (0.95) with model performance decline.
- `transaction_amount` showed a notable increase during the alert months.

### 3. **Anomaly in Transaction Amounts**
- The **monthly average transaction amount** raised an alert at **£3069.8184**.
- Fraudsters may have changed behavior by waiting longer before transacting and making larger transactions.

## Next Steps
- Investigate why `time_since_login_min` impacts fraud detection accuracy.
- Retrain the fraud model with updated data to account for behavior shifts.
- Implement real-time drift detection to adjust model decisions dynamically.

## License
This project is open-source under the **MIT License**.

## Author


---

Feel free to contribute and improve this fraud detection monitoring workflow!

