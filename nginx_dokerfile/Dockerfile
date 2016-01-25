from nginx:latest

maintainer Dockerfiles


run apt-get update
run apt-get install -y supervisor

#configuration nginx
run rm /etc/nginx/conf.d/default.conf
add nginx.conf /root/
run ln -s /root/nginx.conf /etc/nginx/conf.d/
run echo "daemon off;" >> /etc/nginx/nginx.conf

#configuration autostart nginx
add supervisor-app.conf /root/
run ln -s /root/supervisor-app.conf /etc/supervisor/conf.d/

#expose 80
#start nginx after start container
cmd ["supervisord", "-n"]
