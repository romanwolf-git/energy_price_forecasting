## Time Series Forecasting with LSTM

This notebook is part of the work produced within the Melbourne machine learning and AI community's [Green Battery Hack](https://www.mlai.au/hackathon#!). The aim of the hack was to charge and discharge a battery connected to a pv cell connected to the grid, in order to make money by selling energy on the Australian energy market.
![](https://github.com/MLAI-AUS-Inc/gbh-lithiumloaders/blob/f4fdfd8ace6b72beeefa4794531ed90379441944/design/setup.png)

Predicting the price of energy ($/MWh) is therefore essential in deciding what action to take. We decided to use LSTM (Long Short-Term Memory) to predict the price, which is at the core of our larger decision logic. The notebook covers the following steps:

1. **Data Loading and Exploration**: The code loads a CSV file containing time series data and performs basic data exploration and visualization.

2. **Data Cleaning**: Outliers in the data are identified and removed using z-score thresholding. Missing values are imputed using forward filling.

3. **Data Preparation**: The time series data is prepared for the LSTM model by creating a sliding window of past observations as input features and the next observation as the target variable.

4. **Data Scaling**: The input and output data are scaled using the MinMaxScaler to ensure numerical stability during training.

5. **Train-Test Split**: The scaled data is split into training and testing sets.

6. **Model Definition**: An LSTM model is defined using PyTorch, with customizable input size, hidden size, and number of stacked layers.

7. **Model Training**: The LSTM model is trained on the training data using the Adam optimizer and mean squared error loss function. The training process includes periodic validation on the test set.

8. **Model Evaluation**: After training, the model's performance is evaluated on the test set, and visualizations are provided to compare the actual and predicted values.

9. **Model Saving and Loading**: The trained model's state dictionary is saved to a file, and the code demonstrates how to load and use the saved model for inference.

## Usage

To use this code, you'll need to have the following dependencies installed:

- Python 3.x
- PyTorch
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

You can install the required packages using pip:

```
pip install torch numpy pandas matplotlib scikit-learn
```

Once you have the dependencies installed, you can run the Jupyter Notebook and follow along with the code and explanations.

## Acknowledgments
- The `price` data was provided by [opennem](https://opennem.org.au/).

## License

This project is licensed under the [MIT License](LICENSE).
