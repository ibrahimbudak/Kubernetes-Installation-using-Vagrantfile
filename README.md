# Kubernetes-Installation-using-Vagrantfile
## DevOps Project

### Project Requirements

+ Node-Express
+ Docker
+ Docker Registry
+ Jenkins
+ Ubuntu 21.04
+ Dockerhub Account

** _NOTE : All installations mentioned below are done on worker node02._ **

`vagrant up` --> all Clusters are started.<br>
`vagrant status`--> check the status of Clusters<br> 
`vagrant ssh "node name"`-->node by ssh.<br>

![vagrant](https://user-images.githubusercontent.com/42733209/169891496-9482b253-401b-4c9e-9487-96e804f5e1da.png)


## Jenkins Installation 
`sudo apt-get update`<br>
`sudo apt-get install openjdk-8-jdk`<br>
`wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -`<br>
`sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'`<br>
`sudo apt-get update`<br>
`sudo apt-get install jenkins`<br>
https://localhost:8080

![1_fiOou8ZYaZe-Ka8NUyovMw](https://user-images.githubusercontent.com/42733209/169891698-0469019b-d39f-4775-acdc-12db2a33d819.png)


## Create Dockerfile 

Copy the dockerfile to your own dockerfile.

`touch .dockerignore`<br>
`docker build -t node-express:1.0.0`<br>
`docker history node-express:1.0.0`<br>
`docker images`<br>
`docker run -p 3000:3000 node-express:1.0.0`<br>
`docker container ls -a`<br>
`docker commit cb463fd48158 ibrahimbudak/node-express:1.0.0 `<br>
`docker images `<br>
`docker push ibrahimbudak/node-express:1.0.0 `<br>
`docker ps -a `<br>
![Docker-Logo_Horizontel_279x131 b8a5c41e56b77706656d61080f6a0217a3ba356d](https://user-images.githubusercontent.com/42733209/169891616-651a706f-8ca6-4286-baa9-5f2256e5f13e.png)


### Node-Express
`mkdir node-express && cd node-express`<br>
`npm init -y`<br>
`npm i --save express`<br>
`touch index.js`<br>

Add your code to index.js file.

`node index.js`<br>

Check the localhost:3000 address from the browser.

![1_MuVcoMPyJcq8G4qf5s3HGQ](https://user-images.githubusercontent.com/42733209/169891876-a4a80cc5-c8e8-4fa6-bc0b-c3d5008e378e.png)


