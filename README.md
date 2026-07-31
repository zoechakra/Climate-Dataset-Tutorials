# WeatherBench Dataset Tutorial

# 🌦️ WeatherBench Guide

This is a guide to **WeatherBench**, a climate dataset that helps you understand how to use and understand climate data(sets).

## 👋 Who is this guide for?

This guide is designed for those who have completed their first machine learning course.

## ✅ Prerequisites

This guide requires knowledge of **Xarray**, so if you don't have experience with it, this is a good tutorial to check out:

👉 [Xarray in 45 minutes](https://tutorial.xarray.dev/overview/xarray-in-45-min.html)

## 🧭 What you’ll do

You will go through some basic code to understand climate datasets and how to get the data from the dataset.

You will review data visualizations that visualize various types of data:

- 🌍 Geopotential data
- 🌡️ Temperature data
- 🌧️ Precipitation data

Then you will create two models using the climate data we have reviewed.

---

## 🌦️ What is WeatherBench?

WeatherBench is a **"benchmark dataset for data-driven weather forecasting"**.

The data in WeatherBench comes from the **ERA5 reanalysis archive**. ERA5 is a dataset from the **European Centre for Medium-Range Weather Forecasts (ECMWF)**.

More information can be found here:

👉 [ERA5 reanalysis datasets](https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5)

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

👉 [Primitive equations](https://en.wikipedia.org/wiki/Primitive_equations)

However, some simulations of processes require too much computing power, so scientists use approximations.

Weather predictions are highly reliant on these physical models. But the question is:

> 🤖 Can AI also be used to train on past data and predict future weather conditions?

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

## 💾 Dataset Size

The entirety of the **5.625 degree data** has a size of **191 GB**.

Each 3 dimensional variable is roughly **25 GB** each, and the 2 dimensional data has a size of about **2 GB**.

---

## 🔗 Useful Links

- 🌦️ WeatherBench GitHub:  
  [https://github.com/pangeo-data/WeatherBench](https://github.com/pangeo-data/WeatherBench)

- 📚 More information and advanced tutorials:  
  [WeatherBench GitHub](https://github.com/pangeo-data/WeatherBench)

- 📄 WeatherBench research paper:  
  [https://arxiv.org/abs/2002.00469](https://arxiv.org/abs/2002.00469)

- 📝 Blog post summarizing WeatherBench and surrounding information:  
  [https://raspstephan.github.io/blog/weatherbench/#](https://raspstephan.github.io/blog/weatherbench/#)
