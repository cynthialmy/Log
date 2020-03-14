https://blog.panoply.io/cassandra-vs-mongodb


Hadoop writes intermediate results to disk whereas Spark tries to keep data in memory whenever possible.
This makes Spark faster for many use cases.

Apache Pig: SQL-like language the runs on top of Hadoop MapReduce
Apache Hive - another SQL-like interface that runs on top of Hadoop MapReduce

Spark contains libraries for data analysis, machine learning, graph analysis and streaming live data.

Hadoop ecosystem inclydes distributed file storage system HDFS (Hadoop Distributed File System). Spark does not include a file storage system.
Spark can read in data from other sources as well such as Amazon S3.

Spark has streaming library.
Other popular streaming libraries include Storm and Flink.

First dividing up a large dataset and distributing the data across a cluster.
Each data is analyzed and converted into a (key, value) pair.
Then the pairs are shuffle across treh cluster so that all keys are on the same machine.
In the reduce step, the calues with the same keys are combines together.

ETL: extract, transform, load

Machine learning: Logistic Regression, Page Rank. Repetitive funcions running on same data set
Deep learning is not available on SPark because it only supports algorithms that scale linearly with the input data size.
Spark Streaming’s latency is at least 500 milliseconds since it operates on micro-batches of records, instead of processing one record at a time. Native streaming tools such as Storm, Apex, or Flink can push down this latency value and might be more suitable for low-latency applications. Flink and Apex can be used for batch computation as well, so if you're already using them for stream processing, there's no need to add Spark to your stack of technologies.

Another limitation of Spark is its selection of machine learning algorithms. Currently, Spark only supports algorithms that scale linearly with the input data size. In general, deep learning is not available either, though there are many projects integrate Spark with Tensorflow and other deep learning tools.
