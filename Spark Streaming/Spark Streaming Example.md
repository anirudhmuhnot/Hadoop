Spark Streaming Example

Remember to push the uber.csv file in hdfs using
hdfs dfs -mkdir /files
hdfs dfs -copyFromLocal uber.csv(local path) /files/

run the clustering.scala to create a model on historic data on the Google DataProc Cluster.

Then run streaming.scala in another spark-shell.

open connection to port 9998 to the machine on which the above files have been executed. 
Example: code in the above 2 files have been copied and pasted in spark shell of cluster-7478-m 

ssh into another machine worker/master
type the following code
nc -lk cluster-7478-m 9998

now send the uber data in exactly the same format as the input csv and let it predict the cluster id and count using the kmeans on the input data.

