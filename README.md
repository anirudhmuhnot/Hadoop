# Hadoop 2.8.2
wordcount
1) Make new directory in hdfs.
- GOTO dir where bin exists
type - bin/hdfs -mkdir /user
bin/hdfs dfs -mkdir /user/anirudhmuhnot

2)to remove a directory 
bin/hdfs dfs -rmr "/"(this is important) dirname

3)move files into hdfs
bin/hdfs dfs -put (path to file) file/directoryname

4)run the example
bin/hadoop jar libexec/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.8.2.jar wordcount input(input directory name) output(using this saved in the same directory as input)

5)check output
bin/hadoop fs -cat /user/anirudhmuhnot/output/part-r-00000

T3 on Hadoop

access hdfs by:
hdfs dfs -ls /
hdfs dfs <any linux command>

Mapper 
Reducer 
Combiner

FOR JUYPTER NOTEBOOK
gcloud compute ssh "cluster-7478-m" --project moonlit-rock-197404 --zone='us-east1-b' -- -D 10000 -N

/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome "http://cluster-7478-m:8123" --proxy-server="socks5://localhost:10000" --host-resolver-rules="MAP * 0.0.0.0 , EXCLUDE localhost" --user-data-dir=/tmp/

FOR HIVE Create table from hdfs
create external table HVAC(Dateof date,Timeof String, TargetTemp tinyint,ActualTemp tinyint,System tinyint,SystemAge tinyint,BuildingID tinyint)
  row format serde 'org.apache.hadoop.hive.serde2.OpenCSVSerde'
  stored as textfile
location '/csv/';

YARN
hadoop 1.0 only had MapR - had JobTracker and TaskTracker
hadoop 2.0 why only mapR? If someone tries to build their own computation engine. like Job and Task Tracker
It has Resource -master
task tracker - worker nodes

Application manager deals with application after initialisation of resources

SPARK
Spark Job goes to Resource manager of yarn  yarn says this job requires this much resources are required, when workers are free, allocated, yarn gives control of Driver and gives jobs to executors. 

Every dataset is array, in rdd. 
Map changes columns, 

Spark works on multiple file system,like hadoop, HDFS NTFS etc.

SPARK STREAMING
DSTREAM 
abstraction over rdd
So we’ll apply transformation on STREAM and STREAM will apply it on rdd. 

Zepplin



