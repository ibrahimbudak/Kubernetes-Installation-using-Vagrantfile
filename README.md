# Kubernetes-Installation-using-Vagrantfile
## DevOps Project

### Requirements

+ node-express
+ docker
+ Docker Registry

### Node-Express
`mkdir node-express && cd node-express`<br>
`npm init -y`<br>
`npm i --save express`<br>
`touch index.js`<br>

Add your code to index.js file.

`node index.js`<br>

Check the localhost:3000 address from the browser.

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



