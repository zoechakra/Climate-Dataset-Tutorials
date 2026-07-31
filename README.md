# WeatherBench Dataset Tutorial

This is a guide to Weather Bench, a climate dataset that helps you understand how to use and understand climate data(sets).
Who is this guide for: This guide is designed for those who have completed their first machine learning course.
Prerequisites: This guide requires knowledge of Xarray, so if you don't have experience with it, this is a good tutorial to check out: https://tutorial.xarray.dev/overview/xarray-in-45-min.html
You will go through some basic code to understand climate datasets and how to get the data from the dataset. You will review data visualizations that visualize various types of data (geopotential data, temperature data, and precipitation data). Then you will create two models using the climate data we have reviewed.

WeatherBench is a "benchmark dataset for data-driven weather forecasting". The data in WeatherBench comes from the ERA5 reanalysis archive. ERA5 is a dataset from the European Centre for Medium-Range Weather Forecasts (ECMWF). More information can be found here https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5

Traditionally, numerical weather prediction (NWP) is a method used to predict weather. This method solves mathematical equations that describe various physical processes across Earth like air flow. The process involved with these physical models involves understanding physical processes on Earth, representing these Earth system processes with mathematical equations, setting initial conditions, representing changing conditions and then solving these mathematical equations again and again. The equations to start off with are the primitive equations; find out more here: https://en.wikipedia.org/wiki/Primitive_equations However, some simulations of processes require too much computing power so scientists use approximations.

Weather predictions are highly reliant on these physical models. But the question is, can AI also be used to train on past data and predict future weather conditions?

The dataset is made up of hourly data from January 1st, 1979 to December 31st, 2018, over a span of 40 years. WeatherBench has regridded the ERA5 data to lower resolutions as the raw datasets are very large. One vertical level in the raw dataset is around 700 GB worth of data. All the variables we are using are 5.625° (32 latitude values x 64 longitude values) resolution data. This means that the coordinates of the grid differ by 5.625 degrees. Most variable's vertical levels are measured by pressure in hPa.

The entirety of the 5.625 degree data has a size of 191GB. Each 3 dimensional variable is roughly 25GB each and the 2 dimensional data has a size of about 2GB.

This is the github for Weather Bench: https://github.com/pangeo-data/WeatherBench You can find more information about Weather Bench here and find more advanced tutorials. Find the Weather Bench research paper here: https://arxiv.org/abs/2002.00469 Here is a blog post summarizing Weather Bench and surrounding information: https://raspstephan.github.io/blog/weatherbench/#
