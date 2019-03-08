FROM ros:melodic

# RUN apt-get update

ADD . /ros_ws/src/talker/
WORKDIR /ros_ws
RUN /bin/bash -c "source /ros_entrypoint.sh && catkin_make"
RUN chmod +x src/talker/src/talker.py
