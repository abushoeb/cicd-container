# How to run it

```
# clone
git clone 

# install dependencies
npm install

# run application
node app.js

# build docker image
docker build -t youtube-local:latest .

# see the docker image
docker images

# run the container
docker run -it -p 80:3000 <CONTAINER_ID>


# login to aws ecr (prerequisite - make sure aws cli is intalled and loggedin properly )
# aws ecr get-login-password | docker login --username AWS --password-stdin <YOUR-REGISTRY-URL>
aws ecr get-login-password | docker login --username AWS --password-stdin 318409415778.dkr.ecr.us-east-1.amazonaws.com/youtube

# build another docker image
docker build -t youtube:latest . 

# tag the new image
docker tag youtube:latest 318409415778.dkr.ecr.us-east-1.amazonaws.com/youtube:latest

# create vpc and subnet
myvpc 10.0.0.0/16

