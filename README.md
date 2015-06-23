docker-nginx-hhvm-wordpress [![Docker repo](http://img.shields.io/badge/docker-repo-blue.svg)](https://registry.hub.docker.com/u/philipz/nginx-hhvm-wordpress/)
===========================
##Reference

1. https://github.com/CenturyLinkLabs/ctlc-docker-wordpress
2. https://github.com/nikolaplejic/docker.hhvm
3. https://github.com/eugeneware/docker-wordpress-nginx
4. https://github.com/tutumcloud/tutum-docker-wordpress-nosql

##How to use

    docker run -d --name db_1 -e "MYSQL_DATABASE=wordpress" -e "MYSQL_ROOT_PASSWORD=coscup_z>b" -p 3306:3306 ctlc/mysql
    docker run -d --name web_1 --link db_1:db_1 -v $(pwd)/wordpress:/usr/share/nginx/www -e "DB_USER=root" -e "DB_PASSWORD=coscup_z>b" -p 80:80 philipz/nginx-hhvm-wordpress    
