docker run --name mysql -e MYSQL_ROOT_PASSWORD=123456 -e MYSQL_DATABASE=dbdemo -e MYSQL_USER=devspark -e MYSQL_PASSWORD: dev123 -d mysql:5.6


docker build -t webpato . 

docker run --name webpato --link mysql:mysql -d -p 8081:80 -v /home/patriciomase/Docker-training/docker-final-project/worldapi:/opt/www/worldapi webpato
