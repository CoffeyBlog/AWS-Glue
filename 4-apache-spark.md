### Apache Spark

- AWS Glue is built on, or a managed Apache Spark Engine. So, What is Spark?

- Apache Spark is one of the most popular technologies for running big data analysis. It can be up to 100x faster than Hadoop MapReduce

- Big data is data - that for the most part - is too large to fit on one computer

- The way to analyze big data is through distributed computing. The way that distributed computing works is: You have one "Main" node - that is distributing work across a cluster of individual worker nodes.

- The reason to use distributed computing is because one large super computer with 100's of cores is expensive and rare, where as you achieve the same amount of cores with MANY small weaker computers. Another reason is fault tolerance, if one machine across a large network of distributed machines fail ... no big deal. Whereas, if your 1 large 1000 core super-computer fails ... that sucks because you just lost all of your calculations and your data.

### Before we talk about Spark lets talk about Hadoop

- Hadoop was created at Yahoo, it's initial release was 2006 and it's written in Java.

- Hadoop is a way to distribute very large files across multiple machines. It uses (HDFS) Hadoop distributed file system. HDFS allows users to work with large data sets and also duplicates "blocks" of data for fault tolerance.

- The Hadoop HDFS system then also uses a technology called MapReduce which allows computations on that data.

### Hadoop notes

- HDFS will use blocks of data with a size of 128MB by default

- Each of these blocks are replicated 3 times - and those blocks are then distributed in a way to support fault tolerance.

- The smaller blocks provide more parallelization during processing

- Multiple copies of a block prevent loss of data due to failure of a node

- MapReduce is then a way of splitting computation to a distributed set of files such as (HDFS)

- MapReduce consists of a Job tracker and multiple task trackers - (keep this idea of "trackers and jobs in mind when working with Glue and Spark)

- Hadoop is and was a great tool in the days of Yahoo, however 7yrs after Hadoop's realease Spark was released.

### Spark

- Spark was released in 2013, built at AMPLab at UCBerkley and it is written in Scala.

- Spark is blazing fast and case be used as a flexible alternative to MapReduce

- Spark can use many data formats such as Cassandra, S3, HDFS and others.

- Spark is seen as a better alternative (in many cases) to MapReduce, because MapReduce requires that files must be stored in HDFS - Spark does not.

### Spark can also achieve computation up to 100x faster than MapReduce

- It achieves this because MapReduce writes most data to disk after each map and reduce operation. Where as Spark keeps most of the data in memory after each transformation - however Spark can spill over to disk if memory is getting full

### Spark RDD

- At the core of Spark is the idea of a (RDD) Resilient Distributed Dataset

## Resilient Distributed Dataset has 4 main features:

- Distributed collection of data
- Fault tolerance
- Parallel operation - partitioned
- Ability to use many sources

- This system looks very similar to most distributed systems where you have a Main Node with many worker nodes

- RDD's are immutable, lazily evaluated and cacheable

- There are 2 types of Spark operations: 
- Transformations
- Actions

-