oozie-cronscheduler-examples
============================

Examples of the cron-like scheduler introduced in OOZIE-1306.

Sample usage:
Copy files to local filesystem on your Hadoop cluster.

# Place the files into HDFS.
hdfs dfs -put oozie-newscheduler-examples

# Every 15 minutes sample job:
oozie job -oozie http://nodeX:11000/oozie -config oozie-newscheduler-examples/every-fifteen-minutes/job.properties -run
