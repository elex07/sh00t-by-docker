# sh00t-by-docker
Deploy sh00t by docker. Sh00t is a Testing Environment for Manual Security Testers.

##### Sh00t using Docker Python3 image

1. **Create a build**<br/>
cd sh00t-python3<br/>
docker build -t sh00t:latest .

2. **Run Container**<br/>
docker run -it -p 8001:8001 sh00t:latest

3. **Open browser and run http://localhost:8001**<br/>
Admin Credentials<br/>
username	:	admin<br/>
password	:	Password@123

##### Sh00t using Docker Ubuntu16.04 image

1. **Create a build**<br/>
cd sh00t-ubuntu16.04<br/>
docker build -t sh00t:ubuntu .

2. **Run Container**<br/>
docker run -it -p 8001:8001 sh00t:ubuntu

3. **Open browser and run http://localhost:8001**<br/>
Admin Credentials<br/>
username	:	admin<br/>
password	:	Password@123


**Note :**<br/>
1. To see the last updated changes, login to the same container. Find the container id using<br/>
docker ps -a<br/>
Now start the container<br/>
docker start f7528650649b<br/>
where f7528650649b is container id.<br/>
Open http://localhost:8001

2. If you are not able to get internet connection inside docker container as you get error 'could not resolve hostname github.com' or similar, add google name server in your resolv.conf file<br/>
cat /etc/resolv.conf<br/>
nameserver 8.8.8.8

