# GUI-APP-In-Docker

This Command is tested in Redhat 8 Operating System

First Check you have docker installed or not
> rpm -q docker-ce

Start your docker engine and make there service enable
>systemctl start docker
>systemctl enable docker

Check the Docker engine status
>systemctl status docker

To Run GUI Apps in Docker 
> docker run -it --name machinelearning --net=host --env="DISPLAY" --volume="$HOME/.Xauthority:/root/.Xauthority:rw" centos:latest

Let's understand this command:
run :- this keyword will launch the container
-it :- this gives interactive terminal
--name :- use to set the name  of container
machinelearning :- it is name name of container, you can give any name
--net=host :- use to launch the container with host network 
--env="Display" :- This is use to share the display of the host to the container
--volume="$HOME/.Xauthority:/root/.Xauthority:rw" :- This is use to share the host X server with the container by creating volume.
