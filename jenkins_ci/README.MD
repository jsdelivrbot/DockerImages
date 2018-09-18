== Jenkins ==

Install Jenkins or run as a docker

	docker run -p 8080:8080 -d --restart=always -p 50000:50000 --name=zmjenkins -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts
	docker logs 1b04cc833dde


* Then access via browser and insert the above password to "Unlock Jenkins"
* Click "Install Suggested Plugins"
* Create First Admin User	(admin, Ca***p)

## Install maven

To install maven inside the jenkins doker image

	docker exec -u root -it 1b04cc833dde bash

Then just ordinary commands

	apt update
	apt install maven
