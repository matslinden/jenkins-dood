## jenkins-dood (docker-outside-of-docker)

Extends the [jenkins/jenkins
image](https://hub.docker.com/r/jenkins/jenkins/) with
docker-outside-of-docker capabilities.

This enables the use of docker in Jenkins jobs.


### Usage

See the [documentation of the jenkins/jenkins
image](https://github.com/jenkinsci/docker/blob/master/README.md).

To use the docker-outside-of-docker capabilities, add these options to
the docker run command:

    --mount type=bind,source=/var/run/docker.sock,destination=/var/run/docker.sock

    --group-add "$(getent group docker | cut -d: -f3)"


### License

The files in the docker context (the github repo) are licensed
according to its LICENSE file.

As with all Docker images, these likely also contain other software
which may be under other licenses (such as Bash, etc from the base
distribution, along with any direct or indirect dependencies of the
primary software being contained).

As for any pre-built image usage, it is the image user's
responsibility to ensure that any use of this image complies with any
relevant licenses for all software contained within.
