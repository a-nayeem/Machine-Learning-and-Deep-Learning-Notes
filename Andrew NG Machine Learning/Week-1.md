
## What is Machine Learning?

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

Mathematically speaking our goal is to find a function that can predict the price of house given size of it's living area. In our simple dataset with only 2 variables we can use a straight line as our prediction model to get decent accuracy. Let's name the function we are going to find as "hypothesis function". This hypothesis function can be mathematically represented as h : x --> y so that h(x) predicts price of house with acceptable accuracy. 


**Cost Function**

Now to measure the accuracy of our hypothesis function we need a cost function. We can use the average distance of each point from our hypothesis line as cost function. In this case our aim is to reduce this average distance so as to keep the straight line as close as possible to all the points. ​

