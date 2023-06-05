# jenkins-on-EC2

# Install Jenkins on EC2

There are two methods:

1. Install jenkins directly on OS
 - download the package and install on server
 - create separate Jenkins user on server

2. Run Jenkins as Docker container

This approach is easier as it is less stressful.
All you need is to install docker on the server

  sudo apt update
	sudo apt install docker.io
  
  ![jenkins-start-page](https://github.com/bankolejohn/jenkins-on-EC2/assets/76499525/8f35d803-eb88-4be7-9925-d15bc6287b59)
  
  then use
    docker exec -it <container id> bash
  to access the docker container of jenkins in order to execute commands 
  
  then use 
    cat /var/jenkins_home/secrets/initialAdminPassword
  to retrieve the password
  
  enter the password and continue
  
  click on install suggested plugins
  
  then create your username and password
  
  start using jenkins

