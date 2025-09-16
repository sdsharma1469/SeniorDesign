# SeniorDesign

To run this:

## Setup
Install Docker
Download XQuartz (if on Mac)
Create a Docker account
Run Docker Desktop in the background
Run XQuartz in the background

## Commands

# Allow Docker to connect to your display (Mac only)
cd /
xhost +

# Pull the ROS Jazzy image
docker login
docker pull shaun4k04/ros-jazzy:dev1
docker images   # (you should see the image listed now)

# Create and run a container (Mac)
docker run -it \
    -e DISPLAY=:0 \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    --name ros2JazzyContainer \
    shaun4k04/ros-jazzy:dev1 \
    bash

# Test if this is working
  You should see a prompt like:  
    root@2341896f2f6c:/#    
# Then run:  
  xeyes  

# In a separate terminal, show running containers
docker ps

# To list all containers
docker ps -a
