# ROS Workspace


### install docker on rasp  
please refer to [this blog](https://dev.to/elalemanyo/how-to-install-docker-and-docker-compose-on-raspberry-pi-1mo)
## How to run
  
First, create an account on https://app.husarnet.com/  
get husarnet join code and add it to .env

### start developement node :
```
cd Dooby-car/ROS/dev-node
docker-compose up --build
```
Vnc server will be listening on port 6080  
open a terminal in the desktop environment and run:  
```
cd /app/ros2_ws
. install/setup.sh
ros2 launch dooby_simulation display.launch.py
```

### raspberry pi node : 
```
cd Dooby-car/ROS/pi-node
docker-compose up --build
```
the rasp node runs dooby interface packages  

### server node :
```
cd Dooby-car/ROS/server-node
docker-compose up --build
```
the server node runs "navigation2" stack   
