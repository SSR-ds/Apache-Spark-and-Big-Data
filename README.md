# Apache-Spark-and-Big-Data

Credits - AI Engineering

1) Using DataBricks Community Edition to analyze data and work on the data and to practice Spark. Here we are cleaning the data and removing the null values and pushing them into permanent view Arvato format to perform Exploratory Data Analysis on the dataset.

2) Exploratory Analysis Using Spark and Python. DataBricks gives us various methods to visualize the data through simple commands

3) While Java is the basis for Spark we are installing JVM version 8 or higher to make spark run on google colab. Further, then we install the type of apche spark that we need from the official site. The we install pyarrow to run pandas commands directly on the spark dataframe. Then we check it with a dataset loading through spark commands. findspark package helps in setting up system.path variables so that spark can be initialized.


4) Spark Transformations :
            > Upon Installing Spark in Colab we can read a dataframe and the try to make transformations on it as shown in the file. 
            > Spark is lazy programming and hence it requires show to fetch out the data for us
            > Further the explain concept in spark explains the action function performed in it
            > Every action in spark is done through three basic steps takes raw data, does some transformations and aggregates the data, which can be seen by df.explain()
            

Transformations : If we take spark dataframe the data is partitioned and distributed which makes spark fast for large datasets. Hence there are two types of transformations in                       spark - Resilient Distributed Datasets (RDDs) are fundamental data structure in spark

                  1) Narrow : child RDD will refer to only one parent RDD (union)
                  2) Wide : child RDD will refer to multiple parent RDD (groupBy)
  
 Map function : will create tuple for each element - can be said as one to one transformation
 FlatMap function : will no create tuple for each element and everything will be displayed in a list - can be said as one to many
 
Sort and OrderBy are more costlier transformations, hence we can use SortWithinPartitions that would sort by partitions and we can also use multiple columns in that instead of using one column

approxQuantile - to get Quantiles in the dataset, more the confidence interval, more the time it is going to take


5) Reading data into databricks to do analysis with spark from S3 buckets in AWS. 
     > Create a bucket, load in the files inside the bucket
     > Create an IAM Access with necessary access and permissions
     > Once the permissions is granted copy the access key and secret key
     > Use the command line to read in the file inside the databricks 
     > Check for the spacing and check if the file is read properly or else use 
            >  .option("multiline","true") to give a multiline options 

