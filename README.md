# ubuntu start server
 Nodejs, nginx and strapi
# build nodejs
sudo apt update
cd ~
apt install curl
curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh

sudo apt install build-essential
nodejs -v
npm -v
# install git
cd ~
apt install git

# install mysql-server
cd ~
sudo apt-get update
sudo apt-get install mysql-server
mysql -u root -p
create database strapi1;
use strapi1;
exit
# install nginx
cd ~
sudo apt-get install nginx

