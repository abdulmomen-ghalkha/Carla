# Position and Camera-Aided Beam Prediction Using the DeepSense 6G Dataset
## Overview

This project addresses the problem of position and camera-aided beam prediction using the DeepSense 6G dataset. The dataset provides GPS, distance, and camera data collected in a controlled environment for developing and testing machine learning models aimed at enhancing beamforming in wireless communication systems. By leveraging spatial and visual information, we aim to predict optimal beam directions efficiently.

### Key Objectives:

- **Perform Exploratory Data Analysis (EDA):** Analyze GPS and distance data to uncover key features and insights.
- **Feature Engineering:** Extract and preprocess features from spatial data for effective model training.
- **Beam Prediction Modeling:** Develop a machine learning pipeline for accurate beam prediction using position and visual data.
- **Evaluation and Insights:** Validate the model’s performance and derive insights to enhance wireless communication efficiency.

## Dataset Description

The project utilizes the DeepSense 6G Dataset, specifically tailored for position and camera-aided beam prediction tasks.

### Key Components of the Dataset:

- **GPS Data:** Latitude, longitude, and altitude information for the transmitter (TX) and receiver (RX) locations.
- **Distance Data:** Distances between TX and RX in meters.
- **Camera Data:** Images captured during the experiments for visual context.
- **Beam Indices:** Labels for the optimal beam pairs.

## Methodology

### 1. Exploratory Data Analysis (EDA)

Before diving into modeling, we perform a detailed analysis of the GPS and distance data to:

- **Understand Spatial Features:** Explore the distribution and relationships between TX and RX locations.
- **Identify Key Patterns:** Analyze how distance and relative positions influence beam selection.
- **Visualize Spatial Relationships:** Use scatter plots, heatmaps, and other tools to visualize GPS coordinates and distances.

### 2. Feature Engineering

Using insights from the EDA phase, relevant features are engineered, including:

- **Relative Coordinates:** Calculate the relative positions of RX with respect to TX.
- **Distance Metrics:** Include both direct distances and angular differences.
- **Visual Features:** Extract features from camera images using pre-trained models (e.g., ResNet) for downstream prediction.

### 3. Beam Prediction Modeling

We build a supervised learning pipeline using position and visual features:

- **Model Selection:** Start with baseline models (e.g., Random Forest, SVM) and progress to deep learning models (e.g., CNNs, RNNs) for multimodal data.
- **Data Splitting:** Use stratified train-test splits to ensure balanced beam indices across subsets.
- **Hyperparameter Tuning:** Optimize models for accuracy and robustness.

### 4. Evaluation Metrics

Evaluate the models using:

- **Accuracy:** Percentage of correctly predicted beams.
- **Top-k Accuracy:** Evaluate if the correct beam is within the top-k predictions.

## Installation and Setup

To replicate the project, ensure the following dependencies are installed:

- Python (3.8 or later)
- TensorFlow / PyTorch
- Pandas, NumPy, Matplotlib, Seaborn

## References

- [DeepSense 6G Dataset for Position and Camera-Aided Beam Prediction](https://www.wi-lab.net/research/drone-beam-prediction-paper/)

