# BAMBOO CI server :

This document shows the steps to create a Bamboo CI server using DOCKER image.

Step 1 : Go to docker hub and get the official BAMBOO docker image

Step 2 : Create DOCKER volume to store data volume</br>
  $> docker volume create --name bambooVolume

Step 3 : Run the docker run command in detached mode</br>
  $> docker run -v bambooVolume:/var/atlassian/application-data/bamboo --name="bamboo" --init -d -p 54663:54663 -p 8085:8085 atlassian/bamboo-server

Step 4 : Once docker container is up, Bamboo is available in Bamboo is now available on http://localhost:8085*.

Step 5 : Create Login

Step 6 : Need to get trail license, valid for 90 days.

Step 7 : Configure first project and add plan with task to get code repository

Step 8 : Isolate build using Agent environment

Step 9 : Creat Project and First Plan, add task to it.

Step 10 : Configuration as code, you can manage the plan configuration with bamboo specs

Step 11 : To start and stop BAMBOO Bamboo CI Server</br>
  $> docker start bamboo
  $> docker stop bamboo
