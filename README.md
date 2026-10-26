
# Machine Learning-Based Water Leak Detection Using Sensor Data

## Project Overview

This project uses Machine Learning to detect possible water leakage events from sensor data collected from a water distribution testbed. It compares different classification models to identify which performs best at distinguishing normal records from leakage-event records.

## Dataset

**Dataset:** WDSEventDB — A Real-Time Benchmark Dataset for Event Diagnosis in Water Distribution Networks

- **Dataset link:** https://zenodo.org/records/17547955
- **GitHub repository:** https://github.com/Moazeni-s-Concise-Lab/WDSEventDB
- **Licence:** CC BY 4.0, as specified in the dataset record.

The dataset contains sensor measurements such as pressure, water flow, variable-frequency drive (VFD) readings, and analogue valve readings.

This project uses clean operating data and three leakage-event files.

- **Class 0:** Normal or clean record
- **Class 1:** Leakage-event record

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib and Seaborn (if used in the notebook)
- Google Colab / Jupyter Notebook

## Machine Learning Models

1. **Dummy Classifier:** Provides a baseline for comparison.
2. **Logistic Regression:** Learns relationships between sensor readings and class labels.
3. **Random Forest:** Combines multiple decision trees to identify patterns in sensor data.

## Results

The following are the reported test results. Run the notebook to verify them before submission.

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Dummy Classifier | 78.93% | 0.00 | 0.00 | 0.00 |
| Logistic Regression | 78.93% | 0.00 | 0.00 | 0.00 |
| Random Forest | 94.79% | 0.8579 | 0.9023 | 0.8796 |

**Best-performing model:** Random Forest, based on the reported test results.

## How to Run

1. Download the dataset from the [official WDSEventDB page](https://zenodo.org/records/17547955).
2. Open the project notebook in Google Colab or Jupyter Notebook.
3. Upload the required dataset files or configure the file paths used in the notebook.
4. Install any missing dependencies.
5. Run all notebook cells in order to train the models and evaluate their performance.

Install the main dependencies using:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn openpyxl jupyter
```

## Limitations

- The dataset comes from a laboratory testbed.
- Logistic Regression failed to identify leakage records in the reported test results.
- The model does not predict the exact location or size of a leak.
- Further testing on independent and real-world data is required.

## Reference

Raza, N., Iwakin, O., Vilacres, D., Putri, S. A., and Moazeni, F., "WDSEventDB: A Real-Time Benchmark Dataset for Event Diagnosis in Water Distribution Networks," Zenodo, 2025.

https://doi.org/10.5281/zenodo.17547955
