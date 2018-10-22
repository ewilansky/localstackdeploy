# LocalStackDeploy  

## (two scenarios)

This is a small test of stack deploy from Jenkins running in a container and calling docker stack deploy command on a docker host. It doesn't work when called from Jenkins and using the Jenkins Docker plugin.

## Requirements

1. You must have at least Docker CE installed and it must include Kubernetes integration. I'm using version 18.06.1-ce-mac73 (26764).
2. Enable Kubernetes from Docker > Preferences > Kubernetes > Enable Kubernetes checkbox then select Kubernetes for the Orchestration type.
3. Clone this repo.

## Setup

1. Change to the cloned directory and run: docker-compose up -d to start the Jenkins container and return to the commandline. Once the image is pulled, the jenkins_home directory will get created and populated automatically.

2. After the Jenkins container has fully initialized, browse to localhost:8080 and follow the Jenkins instructions for configuring Jenkins and logging-on. The default set of suggested plugins are sufficient to run this test.

3. Connect to the github repository from Jenkins to have Jenkins read the JenkinsFile definition.

### Run the test

Follow this stackoverflow post for testing two scenarios:

- running docker stack deploy from the docker host
- running stack deploy from the Jenkins container

https://stackoverflow.com/questions/52920540/it-is-possible-to-to-call-docker-stack-deploy-on-a-docker-host-from-within-a-jen