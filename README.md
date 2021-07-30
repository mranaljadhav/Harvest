#  Data Science Harvest : Project Overview 

A simple ML and DL based website which recommends the best crop to grow and the diseases caught by your crops.

Farming is one of the major sectors that influences a country’s economic growth.

In country like India, majority of the population is dependent on agriculture for their livelihood. Many new technologies, such as Machine Learning and Deep Learning, are being implemented into agriculture so that it is easier for farmers to grow and maximize their yield.

In this project, I present a website in which the following applications are implemented; Crop recommendation and Plant disease prediction, respectively.

In the crop recommendation application, the user can provide the soil data from their side and the application will predict which crop should the user grow.

For the  plant disease prediction application, the user can input an image of a diseased plant leaf, and the application will predict what disease it is and will also give a little background about the disease and suggestions to cure it.


## Methodology

### What is NPK and Why is it Important?

So now that you know what the numbers on fertilizer mean, you need to know why NPK is important to your plants. All plants need nitrogen, phosphorus, and potassium to grow. Without enough of any one of these nutrients, a plant will fail. 

<b>Nitrogen (N)</b> – Nitrogen is largely responsible for the growth of leaves on the plant. 

<b>Phosphorus (P)</b> – Phosphorus is largely responsible for root growth and flower and fruit development. 

<b>Potassium (K)</b> – Potassium is a nutrient that helps the overall functions of the plant perform correctly.

Knowing the NPK values of a fertilizer can help you select one that is appropriate for the type of plant you are growing. 

For example, if you are growing leafy vegetables, you may want to apply a fertilizer that has a higher nitrogen number to encourage leafy growth. 

If you are growing flowers, you may want to apply a fertilizer that has a higher phosphorus number to encourage more blooms. Before you apply fertilizer to your garden beds, you should have your soil tested. This will also help you determine what balance of fertilizer numbers will be appropriate for your garden’s soil needs and deficiencies.

Read more at Gardening Know How: Fertilizer Numbers – What Is NPK https://www.gardeningknowhow.com/garden-how-to/soil-fertilizers/fertilizer-numbers-npk.htm

## Objective

It is used to help and make easier for farmers to grow and maximize their yield by recommending the best crop to grow and the diseases caught by your crops.

## Code and Resources Used 

**Python Version:** 3.8

**For Web Framework Requirements:** Django

## Install

This project requires Python 3.6 and the following libraries installed:
- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [seaborn](https://seaborn.pydata.org/)
- [tensorflow](https://www.tensorflow.org/)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://ipython.org/notebook.html)

If you do not have Python installed yet, it is highly recommended that you install the [Anaconda](http://continuum.io/downloads) distribution of Python, which already has the above packages and more included.

## Quick Demo

### Homepage 

![demo](https://media.giphy.com/media/Pq0HhPiXEW8Yt8v6Yc/giphy.gif)


### Crop Recommendation

![demo](https://media.giphy.com/media/lDRZUTSulWOWvec6FW/giphy.gif)


### Plant Disease Detection

![demo](https://media.giphy.com/media/PTDgdma07tPDHKxRFm/giphy.gif)

## Data Collection:

The data has been made publicly available on https://www.kaggle.com/atharvaingle/crop-recommendation-dataset for Crop Recommendation Dataset and https://www.kaggle.com/vipoooool/new-plant-diseases-dataset for Plant Diseases Dataset.

## Data Cleaning

After scraping the data, I needed to clean it up so that it was usable for our model. I seen the data is already clean.

## Data Preprocessing

In this stage, I looked at the data of Plant Diseases and find that images are should be converted into array to predict the diseases of plants .

## Model Building 

First, I split the data into train and tests sets with a test size of 20%.   

I tried  different models and evaluated them using Mean Absolute Error. I chose MAE because it is relatively easy to interpret and outliers aren’t particularly bad in for this type of model.   

I tried different models:
*	**Logistic Regressor** 
*	**CatBoost Classifier** 
*	**Random Forest Classifier** 
* **XGB Classifier** 
* **AdaBoost Classifier** 

## Model performance
The Random Forest model far outperformed the other approaches on the validation sets. 
*	**Random Forest Classifier** : Accuracy = 0.99
*	**Logistic Regressor**: Accuracy = 0.95
*	**CatBoost Classifier**: Accuracy = 0.98

## Model Deployement
In this step, I built a django application to deploy the machine learning model that was hosted on a local webserver. The application endpoint takes in a request with a list of values from a interface  listing and returns an estimated value. 

<div align="center">
  <br>
  <br>
  <h3>Happy Coding ✌</h3>
</div>
