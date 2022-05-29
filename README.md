Data analysis of car database  

Data Analysis or sometimes referred to as exploratory data analysis (EDA) is one of the core components of data science. It is also the part on which data scientists, data engineers and data analysts spend their majority of the time which makes it extremely important in the field of data science. This repository demonstartes some common exploratory data analysis methods and techniques using python. For purpose of illustration the [CARS.csv](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793822/CARS.csv)
 has been taken from internet since it is one of the ideal dataset for performing EDA and taking a step towards the most amazing and interesting field of data science.

DataSet Overview

1- The dataset is taken from Internet  and contains details of the cars.

2-The dataset is not clean and hence a lot of data cleaning is carried out. For e.g. prices where too high which are replaced by the median and outliers are removed accordingly.

3-The dataset is cleaned and stored in a CleanData folder which contains the entire cleaned dataset and files structures containing subsets of the cleaned dataset based on Make of the vehicles and vehicle Model.

<img width="877" alt="img" src="https://user-images.githubusercontent.com/89958567/170879214-9c064c01-5532-4fc9-80b1-077e49fec646.png">

More Info and Conclusion : 

The main folder contains 7 folders.

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


After using the technique  the MSRP box plot contains no outlier points this is a big improvement. Previously there were over 15 points of outliers now It have removed those outliers.


ANALYSIS 3

[ANALYSIS_3_CARS data.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793750/ANALYSIS_3_CARS.data.zip)

[Plots.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793752/Plots.zip)

PLOTTING GRAPHS AND COMPARING THEM WITH THEIR ENGINE SIZE,PRICE,TYPE


Here we saw hat , SUV's Sedans seems to be the dominating car types

After plotting the boxplot between the price and the type Clear that Car body type strongly affect the price. 

Now we check cars by EngineSize by plotting a graph. The resukts shows that most of the cars have engine size 3. It means that most of the car have good engine size making the car capacity great.

After that We checked the Horsepower of cars which concluded that mostly cars have horsepower between 200 to 210. 

Then Performed a 5 number summary (min, lower quartile, median, upper quartile, max)

Next step is to perform a 5-number summary for the numeric data. As discussed earlier the numeric data, in this case, are MSRP, Engine Size, Horsepower, Cylinders, Horsepower, MPG_City, MPG_Highway, Weight, Wheelbase, and Length. The five-number summary includes minimum, lower quartile, median, upper quartile, and the maximum values all these values can be obtained by using the describe method.

ANALYSIS 4

[ANALYSIS_4_CARS data.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793767/ANALYSIS_4_CARS.data.zip)

[Plots.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793768/Plots.zip)

PLOTTING GRAPHS AND COMPARING THEM WITH THEIR ENGINE SIZE,PRICE,TYPE

Histogram

Histogram refers to the frequency of occurrence of variables in an interval. Here, there are mainly 10 different car manufacturing companies, but it is often important to know who has the maximum number of cars. I'm just plotting histograms to find the total number of car manufacturers and this plot does not support my predictions or doesn't have relations with the price feature. Plotting a histogram is one of a trivial solution which lets us know the total number of different car manufacturers. From the histogram below it can be seen that Ford has almost several cars (20) followed by Chevrolet (19) and many more.

![Histogram of cars by make](https://user-images.githubusercontent.com/89958567/170880609-6a1825f5-96b0-46ab-a0c4-5af16766b63a.png)

Heat Maps

Heat Maps is a plot which is necessary when we need to find the dependent variables. One of the best ways to find the correlation between the features can be done using heat maps. As shown below the price feature (MSRP) has a strong correlation with Horsepower of 83% this is very important because the more the relationship between the variables the more accurate the model will be. This is how the correlation between the features can be found using heat maps. With the help of heat maps I can use these related features in building my model.

![Heat map](https://user-images.githubusercontent.com/89958567/170880625-b224e7cd-55d2-42da-9139-819341c382bf.png)

Made Scatterplot between two related varirables which concluded that Horsepower of car seems to be highly related to car price. Here the scatter plots are plotted between Horsepower and MSRP are as shown below. With the plot given below, we can easily draw a trend line during modeling. I can easily see a line of best fit in the plot. I have not included the scatter plot between MSRP and Engine Size or Cylinders the reason for this is that these data have comparatively less correlation with the MSRP than that of MSRP and Horsepower which is 83%. Because as seen above the correlation between MSRP and Engine Size is of 57% and that of MSRP and Cylinders is of 65% .


ANALYSIS 5

[ANALYSIS_5_CARS_data.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793784/ANALYSIS_5_CARS_data.zip)

[Box plot of MPG_City.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793786/Box.plot.of.MPG_City.zip)

Here, we performed Univariate Analysis and Bivariant Analysis of the Dataset. By plotting didderent graph we analysed in Univariant Anaysis that :


Most of the cars have the Engine size from 2 to 3

Most of the cars have wheelbase from 100 to 110

Most of the cars have the Weight from 3000 to 4000

Most of the cars have the Horsepower from 150 to 200

Most of the cars have the MSRP from 25000 to 50000.

Then finding the Correlational Matrix 

![Correlation matrix](https://user-images.githubusercontent.com/89958567/170880885-6f470253-66bc-4507-b63a-255d1f975bbf.png)

Aftern that by performing the grapg between Car Make and MSRP it is shown that Price od Merecedes followed by Porshe and Jagaur is high as compared to other cars. Then after that throught Boxplot it showed Type of sports is high in price. Mostly cars have the Origin Europe.  


ANALYSIS 6

[ANALYSIS_6_CARS_data.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793851/ANALYSIS_6_CARS_data.zip)

[Clustering 1.zip](https://github.com/mahakbafna/Data-Ananlysis-in-Python/files/8793852/Clustering.1.zip)


Clustering

The type of clustering used here is k-means clustering k-means clustering is a method of vector quantization, originally from signal processing, that aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean (cluster centers or cluster centroid), serving as a prototype of the cluster. This results in a partitioning of the data space into Voronoi cells. k-means clustering minimizes within-cluster variances (squared Euclidean distances)

Created Clusters

Then checked some scatter plots but with adding cluster.

We can see that clusters speration in power is stronger than mileage which almost have no separation of clusters

I think there is a high relationship between the MSRP (Price) and the Horsepower feature of the car. 

