**PART 1- Multivariate LSTM deep learning model to predict streamflow**
<br><br>
$My Background:$  

I am data scientist working with NOAA to develop a hydrologic modeling tool named t-route, a dynamic channel routing model that is part of the National Water Model (NWM). This model provides a comprehensive solution for river network routing challenges. More detail can be found in [github](https://github.com/AminTorabi-NOAA/t-route/tree/master).
<br><br>
$Introduction:$

This article will be 2 parts, in first part we will go through accessing observed USGS data for a specific point (Brays Bayou, TX) and obtaining meteorological data for hydrologic modeling using Google Earth Engine (GEE). In this Part, we will train and tune hyper parameter of a Long-Short-Term Memory (LSTM) model to simulate streamflow. In Part 2, we will train transformers and ultimately compare the results with t-route (link above).
  
Here's the roadmap for our journey:
1. **Initialization and Data Retrieval:** 
  - Initializes the Earth Engine, 
  - fetches USGS water data, 
  - and processes the response to create a usable DataFrame.
2. **Mapping and Visualization:** 
  - Creates a folium map to visualize the location and surrounding basin.
3. **Fetching ERA5 Data:** 
  - Retrieves ERA5 meteorological data and processes it into a DataFrame.
4. **Data Preparation:** 
  - Prepares the combined dataset for LSTM model input using a custom function.
5. **Building and Training the LSTM Model:** 
  - Defines, builds, trains and tune the LSTM model using TensorFlow and Keras.
6. **Evaluation and Visualization:** 
  - Evaluates the model’s performance and visualizes the results using matplotlib.

This study is inspired by [this](https://nbviewer.org/github/biplovbhandari/tensorflow-ml-models/blob/master/Hydrological_Modeling_using_GEE_and_LSTM.ipynb?flush_cache=True) notebook, However the hyper parameter here is tuned and another model will be added in future and compare with t-route
  <br><br>



