Data analysis of used car database  

Data Analysis or sometimes referred to as exploratory data analysis (EDA) is one of the core components of data science. It is also the part on which data scientists, data engineers and data analysts spend their majority of the time which makes it extremely important in the field of data science. This repository demonstartes some common exploratory data analysis methods and techniques using python. For purpose of illustration the car database dataset has been taken from internet since it is one of the ideal dataset for performing EDA and taking a step towards the most amazing and interesting field of data science.

DataSet Overview

1- The dataset is taken from Internet  and contains details of the cars.

2-The dataset is not clean and hence a lot of data cleaning is carried out. For e.g. prices where too high which are replaced by the median and outliers are removed accordingly.

3-The dataset is cleaned and stored in a CleanData folder which contains the entire cleaned dataset and files structures containing subsets of the cleaned dataset based on Make of the vehicles and vehicle Model.

<img width="877" alt="img" src="https://user-images.githubusercontent.com/89958567/170879214-9c064c01-5532-4fc9-80b1-077e49fec646.png">

More Info
The main folder contains 9 folders.

1- Folders from Analysis1 - Analysis 6 contain the Goolge Colab Notebook, python scripts along with the Plots for that analysis.

2-Data for Analysis folder contains the clean dataset and subsets of data as per the file structure.



ANALYSIS 1

[ANALYSIS_1_CARS_Data.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793715/ANALYSIS_1_CARS_Data.zip)

In this Analysis we are Cleaning the data .

Output for every steps in Cleaning is shown. Steps are as follows:

1- Checking the types of data.

2- Dropping the duplicate rows.

3- Removing the duplicate data.

4- Dropping the missing or null values.


ANALYSIS 2

[ANALYSIS_2_CARS_data.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793744/ANALYSIS_2_CARS_data.zip)

[Plots.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793745/Plots.zip)

DETECTING OUTLINERS AND PLOTTING BOXPLOT

Detecting Outliers

An outlier is a point or set of points different from other points. Sometimes they can be very high or very low. It’s often a good idea to detect and remove the outliers. Because outliers are one of the primary reasons for resulting in a less accurate model. Hence it’s a good idea to remove them. I will perform the IQR score technique to detect and remove the outliers. Often outliers can be seen with visualizations using a box plot. Shown below is the box plot of MSRP. In the plot, you can find some points are outside the box they are none other than outliers.
![Boxplot1](https://user-images.githubusercontent.com/89958567/170880123-4adeda52-2d06-494c-9130-20c28bb51c7d.png)

After using the technique now as seen below the MSRP box plot contains no outlier points this is a big improvement. Previously there were over 15 points of outliers now I have removed those outliers.

![Boxplot2](https://user-images.githubusercontent.com/89958567/170880157-100a2ba1-045f-4249-b03f-0e7974d85ffb.png)

ANALYSIS 3

[ANALYSIS_3_CARS data.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793750/ANALYSIS_3_CARS.data.zip)

[Plots.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793752/Plots.zip)

PLOTTING GRAPHS AND COMPARING THEM WITH THEIR ENGINE SIZE,PRICE,TYPE

![Grapgh of cars by type](https://user-images.githubusercontent.com/89958567/170880285-70f80df0-8524-41df-a4c5-8516b91bc751.png)

SUV's Sedans seems to be the dominating car types

![Box plot of Price of Every typepng](https://user-images.githubusercontent.com/89958567/170880314-79609ba5-1b46-47d7-a0ec-61905bfd9eb0.png)

It's Clear that Car body type strongly affect the price

Now we check cars by EngineSize

![Cars count by engine sixe](https://user-images.githubusercontent.com/89958567/170880326-38854f30-e49d-4753-94b2-88b408223b39.png)


Mostly cars have engine size 3

Now We check the Horsepower of cars

![Horsepwer of cars](https://user-images.githubusercontent.com/89958567/170880375-d772c00f-f43b-4b7b-b44e-f254bf6b8f9d.png)

Performing a 5 number summary (min, lower quartile, median, upper quartile, max)

Next step is to perform a 5-number summary for the numeric data. As discussed earlier the numeric data, in this case, are MSRP, Engine Size, Horsepower, Cylinders, Horsepower, MPG_City, MPG_Highway, Weight, Wheelbase, and Length. The five-number summary includes minimum, lower quartile, median, upper quartile, and the maximum values all these values can be obtained by using the describe method.

ANALYSIS 4

[ANALYSIS_4_CARS data.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793767/ANALYSIS_4_CARS.data.zip)

[Plots.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793768/Plots.zip)

PLOTTING GRAPHS AND COMPARING THEM WITH THEIR ENGINE SIZE,PRICE,TYPE

Histogram

Histogram refers to the frequency of occurrence of variables in an interval. Here, there are mainly 10 different car manufacturing companies, but it is often important to know who has the maximum number of cars. I'm just plotting histograms to find the total number of car manufacturers and this plot does not support my predictions or doesn't have relations with the price feature. Plotting a histogram is one of a trivial solution which lets us know the total number of different car manufacturers. From the histogram below it can be seen that Ford has almost several cars (20) followed by Chevrolet (19) and many more.

![Histogram of cars by make](https://user-images.githubusercontent.com/89958567/170880609-6a1825f5-96b0-46ab-a0c4-5af16766b63a.png)

Heat Maps

Heat Maps is a plot which is necessary when we need to find the dependent variables. One of the best ways to find the correlation between the features can be done using heat maps. As shown below the price feature (MSRP) has a strong correlation with Horsepower of 82% this is very important because the more the relationship between the variables the more accurate the model will be. This is how the correlation between the features can be found using heat maps. With the help of heat maps I can use these related features in building my model.

![Heat map](https://user-images.githubusercontent.com/89958567/170880625-b224e7cd-55d2-42da-9139-819341c382bf.png)

Scatterplot between two related varirables

![Relation Between Horsepower and MSRPpng](https://user-images.githubusercontent.com/89958567/170880637-8c25f4bc-cf16-4b1e-b09f-79b58c4a26f4.png)

Horsepower of car seems to be highly related to car price.

Using more interactive plot to show the previous plot and also adding the car manufacturer

![newplot](https://user-images.githubusercontent.com/89958567/170880702-69535e47-351e-409f-be37-39dc3b7078fa.png)

ANALYSIS 5

[ANALYSIS_5_CARS_data.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793784/ANALYSIS_5_CARS_data.zip)

[Box plot of MPG_City.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793786/Box.plot.of.MPG_City.zip)

Univariate Analysis

![Univariant Analysis](https://user-images.githubusercontent.com/89958567/170880843-fe6bf8e1-6374-4201-a501-844a7da83bb1.png)

Most of the cars have the Engine size from 2 to 3

Most of the cars have wheelbase from 100 to 110

Most of the cars have the Weight from 3000 to 4000

Most of the cars have the Horsepower from 150 to 200

Most of the cars have the MSRP from 25000 to 50000.

Then finding the Correlational Matrix 

![Correlation matrix](https://user-images.githubusercontent.com/89958567/170880885-6f470253-66bc-4507-b63a-255d1f975bbf.png)

Biariant Analysis

Price Analysis with Make

![Boxplot of Price analysis](https://user-images.githubusercontent.com/89958567/170880913-c72e5511-f2c2-44af-8d72-f76b7cdb34d6.png)

Price Analysis with Type

![Boxplot 2](https://user-images.githubusercontent.com/89958567/170880924-7f6e503e-009c-4830-9e1d-e568b797acc5.png)

Catplot of Price with Type of Car

![catplot](https://user-images.githubusercontent.com/89958567/170880946-f246d8a4-b7f0-4133-b3cb-45fc9130e2c7.png)

Catplot of Price with MPG_City of Car

![Box plot of MPG_City](https://user-images.githubusercontent.com/89958567/170880958-eb93acef-7c33-4a80-9b43-dd8306ddaeef.png)

Catplot of Cylinder vs Horsepower

![Catplot 2](https://user-images.githubusercontent.com/89958567/170880969-90cd7267-c191-4793-819f-9e036f71b2b8.png)

Pairplot

![Pairplot](https://user-images.githubusercontent.com/89958567/170880990-233791e3-dc1f-4092-906a-401f0bb2ac4a.png)

ANALYSIS 6

Clustering

The type of clustering used here is k-means clustering k-means clustering is a method of vector quantization, originally from signal processing, that aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean (cluster centers or cluster centroid), serving as a prototype of the cluster. This results in a partitioning of the data space into Voronoi cells. k-means clustering minimizes within-cluster variances (squared Euclidean distances)

Creating Clusters

![Clustering 1](https://user-images.githubusercontent.com/89958567/170881296-f32d3314-0df3-4423-a4d6-bbe2285805b3.png)

![Clustering 2](https://user-images.githubusercontent.com/89958567/170881303-54cef971-2a79-4c09-9665-ff1c2bd920bc.png)

![Clustering 3](https://user-images.githubusercontent.com/89958567/170881312-5f121152-660e-4404-b546-da60637f8713.png)


Now we check some scatter plots but with adding cluster.

But yet we can see that clusters speration in power is stronger than mileage which almost have no separation of clusters

Engine size vs Cylinders


![Scatter plot](https://user-images.githubusercontent.com/89958567/170881330-93072aaf-536b-4909-80ba-7af633b3734f.png)

Now we make an interactive 3D scatter plot of MSRP Horsepower, and EngineSize using also clusters

![newplot (1)](https://user-images.githubusercontent.com/89958567/170881419-db9ec0a3-1aa7-4098-9e4a-f66bf012b2bb.png)


