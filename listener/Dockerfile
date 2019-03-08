FROM ros:melodic

# RUN apt-get update

ADD . /ros_ws/src/listener/
WORKDIR /ros_ws
RUN /bin/bash -c "source /ros_entrypoint.sh && catkin_make"
RUN chmod +x src/listener/src/listener.py