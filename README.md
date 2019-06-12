# sh00t-by-docker
Deploy sh00t by docker. Sh00t is a Testing Environment for Manual Security Testers.

### Sh00t using Docker Python3 image ###

1. ### Create a build
cd sh00t-python3
docker build -t sh00t:latest .

2. ### Run Container
docker run -it -p 8001:8001 sh00t:latest

3. ### Open browser and run http://localhost:8001
Admin Credentials
username	:	admin
password	:	Password@123

### Sh00t using Docker Ubuntu16.04 image ###

1. ### Enter into directory sh00t-with-ubuntu16.04-docker-image and run bulid.
cd sh00t-ubuntu16.04
docker build -t sh00t:ubuntu .

2. ### Run Container
docker run -it -p 8001:8001 sh00t:ubuntu

3. ### Open browser and run http://localhost:8001
Admin Credentials
username	:	admin
password	:	Password@123

##########   ##########   ##########   ##########   ##########   ##########   

Note :
1. To see the last updated changes, login to the same container. Find the container id using
docker ps -a
Now start the container
docker start f7528650649b
where f7528650649b is container id.
Open http://localhost:8001

2. If you are not able to get internet connection inside docker container as you get error 'could not resolve hostname github.com' or similar, add google name server in your resolv.conf file
cat /etc/resolv.conf
nameserver 8.8.8.8

