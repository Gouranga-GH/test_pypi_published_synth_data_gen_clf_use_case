
# Synthetic Data Generator Project

This project demonstrates the use of the `SyntheticDataGenerator` package to generate synthetic datasets for use in machine learning tasks. The project walks through the steps of data collection, preprocessing, model training, evaluation, and the optional addition of noise to simulate real-world data variability.

## Project Overview

The main objective of this project is to showcase how synthetic data can be generated and used to train a simple machine learning model, specifically a Logistic Regression classifier. The project is designed to run in Google Colab.

## Key Features

- Generate continuous, categorical, and time-series synthetic data.
- Use a simple Logistic Regression model to train and test on synthetic data.
- Evaluate model performance using accuracy and classification reports.
- Optionally add noise to the synthetic data and observe the model's performance with noisy data.

## Files

- **Synthetic_Data_Generator_Project.ipynb**: Jupyter notebook demonstrating the complete machine learning workflow using synthetic data.

## Installation

To install the necessary dependencies for this project, run the following commands in your Colab or local environment:

```bash
!pip install --index-url https://test.pypi.org/simple/ synthetic-data-generator
!pip install scikit-learn
```

## Usage

1. **Data Collection**: The notebook generates synthetic data with 2 continuous features and 1 categorical feature.
2. **Data Preprocessing**: The categorical feature is encoded for machine learning use and the dataset is split into training and testing sets.
3. **Model Training**: A Logistic Regression model is trained on the training set.
4. **Model Evaluation**: The model is evaluated on the test set using accuracy and classification reports.
5. **Adding Noise**: Optionally, noise is added to both continuous and categorical data to simulate real-world variability. The model is retrained and re-evaluated on noisy data.

## Example Code

```python
from synthetic_data_generator import SyntheticDataGenerator

# Initialize the synthetic data generator
generator = SyntheticDataGenerator(seed=42)

# Generate synthetic data with 2 continuous features, 1 categorical feature, and 1000 samples
df = generator.create_synthetic_dataset(continuous_features=2, categorical_features=1, num_samples=1000)

# Convert the categorical feature to numerical encoding for machine learning model use
df['categorical_feature_1'] = df['categorical_feature_1'].astype('category').cat.codes
```

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Author

Gouranga Jha
- GitHub: [Gouranga-GH](https://github.com/Gouranga-GH)
- Email: post.gourang@gmail.com
