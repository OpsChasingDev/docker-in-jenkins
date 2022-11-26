> The below information explains how to run Docker within a Jenkins container using persistent Docker volumes in order to pass the Docker binaries from the host server where Docker is installed over to the container running Jenkins (therefore allowing the Jenkins application to make use of Docker commands).  Big thank you to Nancy B. from the Techworld with Nana DevOps Bootcamp course for making this solution!

## Instructions
1. Copy "Dockerfile" and "jenkins_container.sh" into server directory
2. Make sure "jenkins_container.sh" has execute permissions
````
chmod +x jenkins_container.sh
````
3. Build the custom image from the Dockerfile
````
docker build -t jenkins-with-docker
````
4. Start the container from the custom image using the "jenkins_container.sh" script
5. Enter the running container to give all users read/write access to /var/run/docker.sock
````
docker ps
docker exec -it <containerID> -u 0 bash
chmod 666 /var/run/docker.sock
````

## Original Post Information
[Slack link from DevOps Bootcamp](https://techworld-with-nana.slack.com/archives/C01HWAG3WSF/p1663468172211489?thread_ts=1661888090.847439&cid=C01HWAG3WSF)