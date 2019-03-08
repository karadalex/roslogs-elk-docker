ROS Logs & ELK Stack
============================

## How it works

Collect ROS Logs (from ROS Containers) with Filebeat which are then sent to Logstash indexed 
by Elasticsearch and can then be viewed and visualized at Kibana.

All logs are stored in the **roslogs** volume.

## Instructions

```
docker-compose up
```
To run other tools like **rqt_graph** for visualizing the topics you must first set
the ROS_MASTER_URI environment variable. The ros master posrt must match the host port in the
docker-compose file, in this project both host and container ports are 11311. 
If the ros master listens on 11311 then you can skip this step
```
export ROS_MASTER_URI=http://localhost:11311
```
and then run on your **host** machine
```
rosrun rqt_graph rqt_graph
```

## TODO

1. Filter messages in Logstash pipelines