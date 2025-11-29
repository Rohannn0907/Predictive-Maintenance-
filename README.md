# Predictive Maintenance

- This repository contains a machine learning-powered predictive maintenance system designed to assess sensor health. The solution provides a unified report by estimating Remaining Useful Life (RUL), predicting maintenance needs, and detecting anomalous behavior. The entire system is delivered as an interactive, offline-first Streamlit dashboard.

## Key Features

  1. Regression: Estimates the sensor's Remaining Useful Life (RUL) in operational hours.

  2. Classification: Predicts the binary maintenance status ("Normal" vs. "Needs Maintenance").

  3. Clustering (K-Means): Identifies anomalies by analyzing the distance of a data point from normal operating clusters.

  4. Interactive Dashboard: A user-friendly interface built with Streamlit, featuring a five-tab layout for seamless navigation (Home, Historical Data, Input Data, Results,       and Visualizations).

  5. Dynamic Data Input: Allows users to input current sensor readings via interactive sliders or generate random values for testing. All inputs are saved in the session          state for a smooth experience.
  
  6. Rich Visual Analytics: A dedicated tab for data exploration, including histograms, scatter plots, boxplots by maintenance status, a correlation heatmap, and a feature        importance chart for the RUL model.
  
  7. Offline-First Design: Engineered to run entirely on a local machine without any internet dependency, making it suitable for secure and air-gapped environments.

## System Workflow

### The user navigates through a simple, five-step workflow within the application:

- Home: Provides an introduction to the system's goals and explains the three predictive outputs.

- Historical Data: Allows the user to view the complete simulated dataset used for training and validation.

- Input Data: The user enters current sensor values (temperature, vibration, voltage, operational_hours) using sliders.

- Results: The application processes the input and displays the unified health assessment: RUL Prediction, Maintenance Status, and Anomaly    Detection.

- Visualizations: The user can explore various plots to understand the data's underlying patterns and the model's behavior.

## Anomaly Detection Logic

- The system uses a hybrid rule to flag an anomaly. An alert is triggered if either of the following conditions is met:

- The predicted Remaining Useful Life (RUL) is less than 200 hours.

- The data point's distance to its nearest K-Means cluster centroid exceeds the 90th-percentile of historical distances, indicating it's a statistical outlier.

## Technology Stack

- Core Language: Python 3.x
  
- Data Handling: Pandas, NumPy
  
- Machine Learning: Scikit-learn
  
- Web Dashboard: Streamlit, streamlit-option-menu
  
- Scientific Computing: SciPy (for distance calculations)
  
- Data Visualization: Matplotlib, Seaborn
  
- Model Persistence: Pickle

## Getting Started

- Follow these instructions to set up and run the project on your local machine.

## Prerequisites

- Python 3.8 or higher

## Installation

- Clone the repository:
    
    ```bash
    git clone https://github.com/Rohannn0907/Predictive-Maintenance-.git
    cd predictive-maintenance-sensors
    ```

## Create and activate a virtual environment (recommended):

    ```bash
    pip install pipenv
    pipenv shell
    ```
    