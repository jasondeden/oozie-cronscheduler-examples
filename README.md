oozie-cronscheduler-examples
============================

Examples of the cron-like scheduler introduced in OOZIE-1306.

Sample usage:
Copy files to local filesystem on your Hadoop cluster.

# Place the files into HDFS.
hdfs dfs -put coordinator.xml examples/
hdfs dfs -put job.properties.xml examples/
hdfs dfs -put workflow.xml examples/

# Every 15 minutes sample job -- specify the node that your Oozie server is running on:
oozie job -oozie http://nodeX:11000/oozie -config examples/job.properties -run
