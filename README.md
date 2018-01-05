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

