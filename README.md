oozie-cronscheduler-examples
============================

Examples of the cron-like scheduler introduced in OOZIE-1306.

Sample usage:
Copy files to local filesystem on your Hadoop cluster or sandbox.

# Place the files into HDFS.
hadoop fs -put oozie-newscheduler-examples

# Every 15 minutes example:
oozie job -oozie http://localhost:11000/oozie -config oozie-newscheduler-examples/every-fifteen-minutes/job.properties -run

# First day of every month example:
oozie job -oozie http://localhost:11000/oozie -config oozie-newscheduler-examples/first-day-of-the-month/job.properties -run

# Weekdays at 2 am example.
oozie job -oozie http://localhost:11000/oozie -config oozie-newscheduler-examples/weekdays-at-two-am/job.properties -run
