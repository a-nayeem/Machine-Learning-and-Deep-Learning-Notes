
<h1 align="center">Week 1</h1>
<h2>What is Machine Learning</h2>

Machine Learning can be defined in many ways. One simple and informal way to define ML is "the field of study that gives computers the ability to learn without being explicitly programmed."

Let's consider, 

Performance of a program = **P** 

Class of Tasks = **T** 

Experience = **E**

In another formal and modern definition, Tom Mitchell describes ML as using Experience(E) to improve performance of the program (P) for a class of task T.


### Different Type of Machine Learning

Generally learning can be divided into different categories depending on the type of data being used for learning. These categories are:
1. Supervised Learning
2. Unsupervised Learning


**1. Supervised Learning:**
Supervised Learning is done using data for which we can assume there is a relationship between input and output. Supervised Learning problems can be categorized as either "Regression" or "Classification" problem based on the type of data.  


Regression: If the prediction output is a continuous value for example price of house in the house price problem, it is a Regression Problem.

Classification: If the prediction output is a discrete value, for example in spam prediction, spam or not spam, it is a Classification Problem.


**Model Representation**


Let's take simple dataset of House price prediction to understand model representation and further examples. In this dataset there are only two variables, the price of house and living area. Our aim is to predict the price of the house given the living area. So, size of living area is the input and price of house is the output. To mathematically represent this data, we can plot it in a graph. Let's plot the living area in x axis and price of the house in y axis.

As we will be using a lot of data to train the model, let x<sup>(i)</sup> be the input variable (living area of house i) and y<sup>(i)</sup> be the output variable (price of houes i) and (i = 1, 2, 3 ... number of house in dataset). We can represent one training example as a pair (x<sup>(i)</sup>, y<sup>(i)</sup>)

Mathematically speaking our goal is to find a function that can predict the price of house given size of it's living area. Our dataset is pretty simple as it has only 2 variables. So, we can use a linear prediction model or simply a straight line and hope to get a decent accuracy. Let's name the linear function we are going to use, to predict house prices as "hypothesis function". This hypothesis function can be mathematically represented as h : x --> y so that h(x) predicts price of house with acceptable accuracy. 


**Cost Function**

Now to measure the accuracy of our hypothesis function we need a cost function. Cost function determines if our hypothesis function is performing good or bad in terms of predicting the house price. If our hypothesis function performs bad we can try to optimize our function to perform better. Higher cost function means less accurate results, and lower cost function means results with higher accuracy. So our aim is to reduce the cost function. In our simple example cost of a single prediction is the difference between the predicted price and original price. However as our hypothesis function is a straight line, cost of the entire straight line can be found by taking the average cost for all known inputs.  ​


Simple mathematical representation of Cost is as following:

**h<sub>θ</sub>​(x<sub>i​</sub>) − y<sub>i</sub>**


Where h<sub>θ</sub>​(x<sub>i​</sub>) is our hypothesis function. To average we can sum the distances of all the results of our hypothesis function for input x, and their actual output y, and then divide the sum by the total number of data we have in dataset.

Let's give our hypothesis function a proper definition. 


If we plot values of J(θ<sub>1</sub>) for different values of θ<sub>1</sub> we will see that the graph looks like the following image:



If we observe the graph we will see that cost function is the lowest when θ<sub>1</sub> = 1, which is the global minima. 


For a function with 2 input variables like J(θ<sub>0</sub>, θ<sub>1</sub>) we can use contour graph to better understand where our global minima is. A contour graph is a way to plot a 3D graph in a 2D plane with constant sices of z axis.


**Gradient Descent**
Now that we have a way to measure performance of our hypothesis function, we need to find way how to optimize our function using the performance measure. 

![alt text](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bn9SyaDIEeav5QpTGIv-Pg_0d06dca3d225f3de8b5a4a7e92254153_Screenshot-2016-11-01-23.48.26.png?expiry=1651622400000&hmac=aErkEYhj2J0B0LjECQzc6stTXVxu16cBHoqFHmZ52ks)


