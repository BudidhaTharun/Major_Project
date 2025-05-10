# Crop Yield Prediction Using GraphSAGE and LSTM

Crop yield prediction is a process of estimating future agricultural yield based on environmental factors. The global demand for food is increasing, requiring better yield predictions. Traditional prediction models often lack the ability to capture spatial and temporal dependencies, which are crucial for accurate forecasting.

This project integrates **GraphSAGE** for spatial analysis and **LSTM** for time-series forecasting to enhance accuracy. By combining these techniques, the model provides better predictions for agricultural planning.

---

## Features

- **Spatial Analysis**: Leverages GraphSAGE to capture spatial dependencies between regions.
- **Temporal Forecasting**: Uses LSTM for time-series predictions of crop yields.
- **Multi-Factor Integration**: Considers climate, soil quality, past yield trends, and geographical data for better accuracy.
- **Real-World Interpretability**: Provides predictions in interpretable units like kg per hectare.

---

## Data Used

1. **Climate Data**: Temperature, Rainfall, and other weather-related data.
2. **Soil Data**: pH value, soil type, nutrient composition, and moisture levels.
3. **Geographical Data**: Latitude, Longitude, and elevation for spatial dependencies.
4. **Crop Data**: Crop type and past yield records.

---

## Methodology

1. **Data Preprocessing**:
   - Cleaning, Normalization, and Feature Selection.
2. **Graph Construction**:
   - Creating spatial graphs using latitude/longitude.
3. **GraphSAGE Embeddings**:
   - Learning node representations from the constructed graph.
4. **LSTM Model**:
   - Predicting yield based on learned embeddings and historical data.
5. **Model Evaluation**:
   - Comparing results with traditional machine learning models.

---

## How It Works

### Graph Neural Networks (GNN) Overview
A Graph Neural Network (GNN) is a type of deep learning model designed to work with graph-structured data. It extends neural networks to graphs by incorporating connectivity information into learning.

- Captures relationships between connected data points.
- Preserves spatial and contextual dependencies within structured data.

### Yield Prediction Pipeline
1. **GraphSAGE**:
   - Generates spatial embeddings to capture relationships between regions.
2. **LSTM**:
   - Uses historical data and embeddings for time-series forecasting.
3. **Regression Function**:
   - Generates final yield predictions using a linear activation function.
4. **Optimization**:
   - Minimizes prediction error using Mean Squared Error (MSE).

---

## Installation and Setup

### Prerequisites
Ensure you have the following installed:
- Python 3.7 or higher
- Google Colab (recommended for running the project)

### Required Libraries
Install the following libraries:
```bash
pip install torch pandas numpy networkx matplotlib
```

---

## How to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/BudidhaTharun/Major_Project.git
   cd crop-yield-prediction
   ```

2. **Load Dataset**:
   - Upload your dataset to Google Colab or provide the dataset path in the script.

3. **Preprocess the Data**:
   - Run the data preprocessing script to clean, normalize, and select relevant features.

4. **Construct the Graph**:
   - Use the geographical data to create a graph structure for spatial analysis.

5. **Train the Model**:
   - Implement GraphSAGE for learning embeddings and LSTM for yield prediction.
   - Run the model training script:
     ```bash
     python train_model.py
     ```

6. **Evaluate the Model**:
   - Compare the results with traditional machine learning models and analyze the metrics.

7. **Make Predictions**:
   - Use the trained model to predict crop yield for new input data.

---

## Outputs
- **Continuous Yield Values**: Provides interpretable predictions, e.g., kg per hectare.
- **Error Minimization**: Optimized using Mean Squared Error (MSE).

---

## Acknowledgments
This project leverages advanced machine learning techniques for addressing real-world agricultural challenges. Special thanks to the developers of GraphSAGE and PyTorch for enabling this work.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
