# unifi-controller-docker-compose
My code for running Unifi controller as a docker container with persistent storage for data

It is a result of my struggles with deploying a container with persistent storage to store the Unifi Controller data (as earlier I used to rely on manual backups and download/restore after every firmware upgrade).

With this code, the life is pretty simple.

To get going with deploying the container, here are the steps:

1. Install docer on your host : https://docs.docker.com/get-docker/
2. Install portainer : https://documentation.portainer.io/v2.0/deploy/linux/
3. Log into portainer, click and enter into your docker host
4. Go to Stacks> Add Stack
5. Name your stack
6. Copy the given code into the web editor
7. Deploy the stack
8. Kick back and relax, it ill take a few minutes to set up (dependant on your internet speed/host specs)
9. All done - access your unifi controller as a first time user through the <docker host IP>:8080 [port 8080]
  
To upgrage your existing controller to the latest version
1. Log into portainer
2. Stop the unifi-controller container CAUTION: DO NOT REMOVE OR DELETE ANY VOLUMES if asked
3. Remove the unifi controller image
4. Redeploy the stack above and you are good
