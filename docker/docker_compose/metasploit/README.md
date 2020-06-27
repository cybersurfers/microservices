# metasploit and nginx

## This README contains links to installing Docker, Docker Compose, and instructions on running the files located in here. This has been tested on Mac and Linux.

### Step 1: Install Docker
Instructions for installing Docker can be found here:  
https://docs.docker.com/install/

### Step 2: Install Docker Compose
Docker Compose is installed with Docker for Mac. Instructions for installing Docker Compose can be found here:  
https://docs.docker.com/compose/install/

### Step 3: Run docker-compose
Ensure that you are in the same directory as the docker-compose.yml file. Enter the following:  
`docker-compose up -d`  

Enter the following to make sure two containers are running:  
`docker ps`

### Step 4: Enter the metasploit container
Enter the following command:  
`docker exec -it metasploit_metasploit_1 /bin/bash`  

You should now be on the metasploit container. You can use all the usual commands that are part of the metasploit framework. The nginx container can be pinged:
`ping 172.28.0.3`

You can also access the nginx container in your host's web browser by navigating to http://localhost:8080

You can also enter the nginx container from your host:
`docker exec -it metasploit_metasploit_1 /bin/bash`

### Step 5: Clean up
To stop the containers enter:  
`docker-compose down`

To delete the images enter:  
`docker rmi metasploitframework/metasploit-framework`  
`docker rmi nginx`
