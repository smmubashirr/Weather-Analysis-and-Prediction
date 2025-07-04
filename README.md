# Weather Analysis and Prediction

## The Dataset

The dataset used in this project contains detailed daily weather observations and was sourced from Kaggle. It includes a variety of meteorological features that describe weather conditions across different days. These features capture temperature, humidity, pressure, visibility, wind information, and summary descriptions of the day's weather.

The dataset contains the following columns:

* `Formatted Date:` Timestamp of the observation
* `Summary:` Short description of the weather condition
* `Precip Type:` Type of precipitation (e.g., rain, snow)
* `Temperature (C):` Measured temperature in Celsius
* `Apparent Temperature (C):` Perceived or "feels-like" temperature in Celsius
* `Humidity:` Relative humidity (scale of 0 to 1)
* `Wind Speed (km/h):` Wind speed in kilometers per hour
* `Wind Bearing (degrees):` Wind direction in degrees
* `Visibility (km):` Visibility distance in kilometers
* `Loud Cover:` Cloud cover value (usually between 0 and 1)
* `Pressure (millibars):` Atmospheric pressure measured in millibars
* `Daily Summary:` Detailed textual summary of the day’s weather

The target variable for this project is `Summary`, which represents a short textual description of the weather condition (e.g., *Partly Cloudy*, *Drizzle*, *Clear*). It contains a large number of unique classes, many of which are semantically similar or overlapping. To improve modeling performance and interpretability, the project will explore different strategies to simplify or reduce these classes during preprocessing.

**Dataset Source:** [Kaggle - Weather Dataset](https://www.kaggle.com/datasets/muthuj7/weather-dataset/data)

## Project Description

A project that aims to explore historical weather data to uncover meaningful insights and build machine learning models capable of predicting future weather conditions. The overall goal is to understand patterns within the data and use them to develop robust, generalizable models for classification tasks. To accomplish this, the project will follow a structured pipeline:

- **Data Exploration:** The dataset will be examined in depth to understand its structure, distributions, and potential issues. This includes viewing summary statistics, checking data types, visualizing correlations, and understanding variable distributions.

- **Data Cleaning and Preprocessing:** The raw data will be cleaned by handling missing values, dealing with outliers, removing duplicates, and extracting useful information from date fields. Unnecessary columns will be dropped, and appropriate encoding and scaling techniques will be applied.

- **Target Variable Engineering:** Since the original target variable contains multiple classes, different strategies will be explored to simplify or reduce these classes for better modeling performance and interpretability.

- **Feature Selection:** Permutation-based feature importance will be used to identify and drop less informative features. This step aims to improve the efficiency and accuracy of the models.

- **Model Development:** A range of machine learning models will be trained and evaluated. For each model, various configurations will be tested, starting with default settings, moving to custom hyperparameters, and finally applying hyperparameter tuning.

- **Evaluation and Comparison:** The models will be assessed using consistent metrics across training, validation, and test sets. Their performances will be compared to determine which setup performs best under the defined constraints.

- **User Interface:** A simple command-line interface will be created to allow users to input weather parameters and receive predictions using the best-performing models.

- **Incremental Learning:** The project will also include code to support incremental learning, enabling selected models to update themselves as new data becomes available.
