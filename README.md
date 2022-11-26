## Original Post Information
[Slack link from DevOps Bootcamp](https://techworld-with-nana.slack.com/archives/C01HWAG3WSF/p1663468172211489?thread_ts=1661888090.847439&cid=C01HWAG3WSF)

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
