from ubuntu:14.04

maintainer Dockerfiles

#install
run apt-get update
run apt-get install -y build-essential git
run apt-get install -y curl
#install Nodejs
run curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
run apt-get install -y nodejs

#open port 3000
expose 3000

#start nodejs aftrer start container
cmd cd /data; npm start