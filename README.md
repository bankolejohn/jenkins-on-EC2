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
	
then

	sudo docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts

(note **port 5000** is where the jenkins master and worker node communicates; for large workloads)
(**-v** is to mount volumes fo rdata persistence)
(**jenkins_home** is the path that would be created and referenced by jenkins)
(the data created by jenkins by default is stored in **/var/jenkins_home**)
(**jenkins/jenkins:lts** is the official name of the jenkins image)
  
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
  
  Note:
  
  There are two roles for Jenkins App
  
  1. Jenkins Administrator

- admininisters and manages jenkisn
- sets up jenkins cluster
- install plugins
- backup jenkins data

2. Jenkins User
- creates the actual work flows



