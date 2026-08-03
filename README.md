# 🌦️ WeatherBench Guide

This is a guide to **WeatherBench**, a climate dataset that helps you understand how to use and understand climate data(sets).

## 👋 Who is this guide for?

This guide is designed for those who have completed their first machine learning course.

## ✅ Prerequisites

This guide requires knowledge of **Xarray**, so if you don't have experience with it, this is a good tutorial to check out:

https://tutorial.xarray.dev/overview/xarray-in-45-min.html

## 🧭 What you’ll do

You will go through some basic code to understand climate datasets and how to get the data from the dataset.

You will review data visualizations that visualize various types of data:

- 🌍 Geopotential data
- 🌡️ Temperature data
- 🌧️ Precipitation data

Then you will create machine learning models using the climate data we have reviewed.

You will also explore **time series forecasting models**, where we use past climate data to try and predict future values. Since WeatherBench data is recorded hourly across many years, it is a really good dataset for practicing time series modeling.

Some of the models and strategies explored include:

- 📈 Linear Regression
- 🌲 Random Forest
- 🚀 XGBoost / Extreme Gradient Boosting
- ⏰ Time-based feature engineering
  - hour
  - day of week
  - month
  - year
  - day of year
  - week of year
- 🔁 Lag features, where previous values are used to predict future values
- 🧠 NeuralProphet
- 📊 Autocorrelation and lag plots
- 🧪 Train/test splitting and RMSE model evaluation

---

## 🌦️ What is WeatherBench?

WeatherBench is a **"benchmark dataset for data-driven weather forecasting"**.

The data in WeatherBench comes from the **ERA5 reanalysis archive**. ERA5 is a dataset from the **European Centre for Medium-Range Weather Forecasts (ECMWF)**.

More information can be found here:

https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5

---

## 🧮 Traditional Weather Prediction

Traditionally, **numerical weather prediction (NWP)** is a method used to predict weather.

This method solves mathematical equations that describe various physical processes across Earth, like air flow. The process involved with these physical models involves:

- Understanding physical processes on Earth
- Representing these Earth system processes with mathematical equations
- Setting initial conditions
- Representing changing conditions
- Solving these mathematical equations again and again

The equations to start off with are the **primitive equations**.

Find out more here:

https://en.wikipedia.org/wiki/Primitive_equations

However, some simulations of processes require too much computing power, so scientists use approximations.

Weather predictions are highly reliant on these physical models. But the question is:

🤖 Can AI also be used to train on past data and predict future weather conditions?

This guide looks at that question by using climate data to build models, compare predictions, and understand how time series forecasting can be applied to weather data.

---

## 📦 About the Dataset

The dataset is made up of hourly data from **January 1st, 1979 to December 31st, 2018**, over a span of **40 years**.

WeatherBench has regridded the ERA5 data to lower resolutions, as the raw datasets are very large. One vertical level in the raw dataset is around **700 GB** worth of data.

All the variables we are using are **5.625° resolution data**:

- **32 latitude values**
- **64 longitude values**

This means that the coordinates of the grid differ by **5.625 degrees**.

Most variable's vertical levels are measured by pressure in **hPa**.

---

## 🗂️ Variables You Can Explore

There are many different variables included in the WeatherBench data. For example, for the 5.625 degree data, some variables you can explore include:

- 10m u component of wind
- 10m v component of wind
- 2m temperature
- Constants
- Geopotential
- Geopotential at 500 hPa
- Potential vorticity
- Relative humidity
- Specific humidity
- Temperature
- Temperature at 850 hPa
- TOA incident solar radiation
- Total cloud cover
- Total precipitation
- U component of wind
- V component of wind
- Vorticity

---

## 💾 Dataset Size

The entirety of the **5.625 degree data** has a size of **191 GB**.

Each 3 dimensional variable is roughly **25 GB** each, and the 2 dimensional data has a size of about **2 GB**.

---

## 🤖 Machine Learning + Time Series Models

The machine learning section uses WeatherBench variables to build models that predict climate/weather values.

For example, we use variables such as:

- Geopotential at 500 hPa
- Temperature at 850 hPa
- 2m temperature
- Total precipitation
- Total cloud cover
- Solar radiation

One part of the guide builds a model using multiple climate variables to predict temperature. Another part focuses more on **time series forecasting**, where the data is for a specific location and we use patterns over time to make predictions.

Since the data is hourly, there are many time patterns we can explore, like:

- Daily patterns
- Weekly patterns
- Seasonal patterns
- Yearly trends
- Lagged relationships between previous values and future values

The guide also compares model performance using **RMSE**, which helps us understand how far away our predictions are from the real values.

Some of the models include:

- 📈 **Linear Regression**
- 🌲 **Random Forest**
- 🚀 **XGBoost**
- 🔁 **Lag feature models**
- 🧠 **NeuralProphet**

You will also create time-based features and lag features, which are very useful for forecasting. For example, if we want to predict the next geopotential value, we can use previous geopotential values as inputs.

---

## 🧰 Tools Used

Some libraries and tools used in this guide include:

- **Xarray** — Helps make NetCDF files understandable
- **Pandas** — For dataframes and time series data
- **NumPy** — To understand data values
- **Matplotlib** — For making data visualizations
- **Seaborn** — For visualizing patterns in the data
- **Scikit-learn** — For building machine learning models
- **XGBoost** — For XGBoost regression models
- **sktime** — For time series forecasting
- **skforecast** — For autoregressive forecasting models
- **statsmodels** — For autocorrelation plots and time series tests
- **NeuralProphet** — For forecasting with trend and seasonality
- **SHAP** — For understanding model predictions

---

## 🧭 Navigation Tip

If you are already familiar with getting the data from a dataset and want to skip to the visualizations, go to the **"Visualizing the Data"** sections.

However, make sure to run the code converting longitude values to the **-180 to 180 range** under the **"Understanding the Dataset"** section.

Otherwise, if you want to go straight to the models, skip to the **"Machine Learning Models"** header.

---

## 🔗 Useful Links

- 🌦️ WeatherBench GitHub:  
  https://github.com/pangeo-data/WeatherBench

- 📚 More information and advanced tutorials:  
  https://github.com/pangeo-data/WeatherBench

- 📄 WeatherBench research paper:  
  https://arxiv.org/abs/2002.00469

- 📝 Blog post summarizing WeatherBench and surrounding information:  
  https://raspstephan.github.io/blog/weatherbench/#
