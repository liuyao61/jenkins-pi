# jenkins-pi
Jenkins for Raspberry Pi 3

# create volume for jenkins home

``
docker create -v /var/jenkins_home --name jenkins_data resin/armv7hf-debian /bin/true
``

# run container with the volume

``
docker run -p 8080:8080 --volumes-from jenkins_data --name jenkins -d yaoliu/jenkins
``


# Credit:

https://github.com/joherma1/sia-ci
