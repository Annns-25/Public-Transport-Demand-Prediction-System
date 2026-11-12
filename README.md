# Public-Transport-Demand-Prediction-System
🚌 **Public Transport Demand Prediction System** is a Machine Learning project that predicts passenger demand using historical transport, time, route, and weather data. It uses a **Random Forest Regression model** and provides an interactive **Gradio interface** for real-time demand prediction and service recommendations.
# 🚌 Public Transport Demand Prediction System

### ML-Based Passenger Demand Prediction using Random Forest Regression

An end-to-end **Machine Learning project** that predicts the expected number of passengers in public transportation based on factors such as time, route, weather, holidays, special events, transport mode, and scheduled capacity.

The project includes **data preprocessing, feature engineering, model training, evaluation, and an interactive Gradio prediction interface**.

---

## 📌 Project Overview

Public transport demand changes depending on the time of day, route, weather, holidays, special events, and other factors.

This project uses historical transportation data to predict:

> **How many passengers are expected at a particular time and location?**

The prediction can help transport operators make better decisions about:

* 🚌 Vehicle allocation
* ⏰ Service frequency
* 👥 Passenger capacity planning
* 📊 Demand monitoring
* 🚦 Peak-hour management
* ⚡ Resource optimization

---

## 🎯 Problem Statement

Public transportation systems often face difficulty in accurately estimating passenger demand.

Low demand can result in inefficient resource usage, while unexpectedly high demand can cause overcrowding and insufficient transportation capacity.

Therefore, this project aims to develop a Machine Learning system that predicts passenger demand using historical transportation and environmental data.

---

## 🎯 Objectives

* Predict passenger demand using Machine Learning.
* Analyze factors affecting public transport demand.
* Identify low, medium, and high demand periods.
* Help optimize vehicle and service allocation.
* Provide an easy-to-use prediction interface using Gradio.

---

## 📊 Dataset

The dataset contains transportation records with information about:

| Feature              | Description                  |
| -------------------- | ---------------------------- |
| `record_id`          | Unique record identifier     |
| `timestamp`          | Date and time of the record  |
| `date`               | Date of travel               |
| `hour`               | Hour of the day              |
| `day_of_week`        | Numerical day of week        |
| `day_name`           | Name of the day              |
| `is_weekend`         | Weekend indicator            |
| `is_holiday`         | Holiday indicator            |
| `is_special_event`   | Special event indicator      |
| `is_peak_hour`       | Peak-hour indicator          |
| `route_id`           | Transport route              |
| `transport_mode`     | Bus/Metro/etc.               |
| `stop_name`          | Transport stop               |
| `distance_to_cbd_km` | Distance from CBD            |
| `weather_condition`  | Weather condition            |
| `temperature_c`      | Temperature                  |
| `precipitation_mm`   | Precipitation                |
| `humidity_pct`       | Humidity                     |
| `fare_inr`           | Fare                         |
| `scheduled_capacity` | Scheduled passenger capacity |
| `passenger_count`    | **Target variable**          |
| `occupancy_rate_pct` | Occupancy percentage         |

### 🎯 Target Variable

```text
passenger_count
```

The model predicts the expected number of passengers.

---

## 🤖 Machine Learning Model

### Random Forest Regressor

The project uses **Random Forest Regression** because it can capture complex relationships between multiple transportation, time, and environmental features.

### ML Workflow

```text
Dataset
   ↓
Data Cleaning
   ↓
Feature Engineering
   ↓
Categorical Encoding
   ↓
Train-Test Split
   ↓
Random Forest Regression
   ↓
Model Evaluation
   ↓
Prediction
   ↓
Gradio Interface
```

---

## 🛠️ Technologies Used

* 🐍 Python
* 🐼 Pandas
* 🔢 NumPy
* 🤖 Scikit-learn
* 🎨 Gradio
* 💾 Joblib
* 📓 Jupyter Notebook
* 📊 Matplotlib

---

## 🔧 Data Preprocessing

The project performs the following preprocessing steps:

1. Load the dataset.
2. Check missing values.
3. Clean the dataset.
4. Convert date values into datetime format.
5. Extract:

   * Year
   * Month
   * Day
6. Encode categorical variables using `OneHotEncoder`.
7. Split the dataset into training and testing sets.

---

## 📈 Model Evaluation

The model is evaluated using:

### MAE — Mean Absolute Error

Measures the average difference between actual and predicted passenger counts.

### RMSE — Root Mean Squared Error

Measures prediction error while giving more weight to larger errors.

### R² Score

Shows how well the model explains the variation in passenger demand.

```text
MAE   → Lower is better
RMSE  → Lower is better
R²    → Higher is better
```

---

## 🖥️ Gradio Interface

The project includes an interactive Gradio interface where users can enter transportation details.

### Input Features

* 📅 Date
* 🕐 Hour
* 📆 Day of Week
* 🗓️ Day Name
* Weekend
* Holiday
* Special Event
* Peak Hour
* Route ID
* Transport Mode
* Stop Name
* Distance to CBD
* Weather Condition
* Temperature
* Precipitation
* Humidity
* Fare
* Scheduled Capacity

### Output

The system provides:

```text
Predicted Demand
Demand Level
Recommendation
```

Example:

```text
Predicted Demand: 125 passengers

Demand Level: 🔴 High Demand

Recommendation:
Increase vehicles or service frequency.
```

---

## 🚦 Demand Classification

The system provides a simple demand-level interpretation:

| Passenger Demand | Level     | Recommendation                        |
| ---------------: | --------- | ------------------------------------- |
|           `< 50` | 🟢 Low    | Normal service                        |
|          `50–99` | 🟡 Medium | Consider increasing service frequency |
|          `≥ 100` | 🔴 High   | Increase vehicles/service frequency   |

---

## 📁 Project Structure

```text
Public-Transport-Demand-Prediction/
│
├── 📓 Public_Transport_Demand_Prediction.ipynb
│
├── 📊 public_transport_demand_dataset.csv
│
├── 🤖 public_transport_demand_model.pkl
│
├── 📄 README.md
│
└── 📋 requirements.txt
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Move into the project folder:

```bash
cd Public-Transport-Demand-Prediction
```

Install the required libraries:

```bash
pip install pandas numpy scikit-learn gradio joblib matplotlib
```

---

## ▶️ Running the Project

### 1. Open Jupyter Notebook

```bash
jupyter notebook
```

### 2. Open

```text
Public_Transport_Demand_Prediction.ipynb
```

### 3. Run the cells

Run the notebook from top to bottom.

### 4. Launch Gradio

The final cell launches the interactive application:

```python
demo.launch()
```

The local Gradio application will then be available through the URL shown in the Jupyter output.

---

## 🔮 Future Improvements

Future versions of this project could include:

* 📅 Time-series forecasting
* 🧠 Gradient Boosting / XGBoost comparison
* 📍 Real-time transport data
* 🌦️ Real-time weather information
* 📊 Interactive demand dashboards
* 🚌 Dynamic vehicle allocation
* 📱 Mobile-friendly deployment
* ☁️ Cloud deployment
* 📈 Advanced hyperparameter tuning

---

## 🌍 Real-World Impact

This system can support public transportation planning by helping operators anticipate passenger demand.

Potential benefits include:

* Reduced overcrowding
* Better vehicle utilization
* Improved passenger experience
* More efficient scheduling
* Better peak-hour planning
* Data-driven transportation management

---

## ⚠️ Limitations

* Prediction quality depends on the quality of historical data.
* Unexpected events may affect actual passenger demand.
* The current model does not use live transportation data.
* Weather and special-event information may not always be available in real time.
* The demand thresholds used for recommendations are simplified.

---

## 👨‍💻 Project Type

**Machine Learning — Regression**

### Model

```text
Random Forest Regressor
```

### Target

```text
passenger_count
```

### Interface

```text
Gradio
```

### Development Environment

```text
Jupyter Notebook
```

---

## 📜 License

This project is created for **educational and academic purposes**.

---

## ⭐ Acknowledgement

This project was developed as part of a Machine Learning project to demonstrate the practical application of regression techniques in public transportation demand forecasting.

---

## 🚀 Conclusion

The **Public Transport Demand Prediction System** demonstrates how Machine Learning can be applied to transportation data to estimate passenger demand.

By combining historical transport information, time-based features, route information, weather conditions, and capacity information, the system provides a practical approach to demand prediction and transportation planning.
