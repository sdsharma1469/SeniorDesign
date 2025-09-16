# SeniorDesign
To run this

Install docker 
download xQuartz (if on mac)  
create a docker account  
run docker app in the background  
run xQuartz in the background  

open a terminal and run the following :  
  cd /  
  xhost +   
  (this will allow the docker container to connect to your display)  

in terminal:  
  docker login  
  docker pull shaun4k04/ros-jazzy:dev1   
  docker images   
  (you should see the image listed now)  

on mac :  
  docker run -it \  
      -e DISPLAY=:0 \  
      -v /tmp/.X11-unix:/tmp/.X11-unix \  
      --name ros2JazzyContainer \  
      shaun4k04/ros-jazzy:dev1 \  
      bash  
  (this should create and run a container with the ros image  

to test if this is working :  
  a) should show something like this in the command line   
        root@2341896f2f6c:/#   
  b) run the command :    
        xeyes   

open a separate terminal:  
  docker ps    
  (this should show you your running containers)  

to list all containers:  
  docker ps -a  

