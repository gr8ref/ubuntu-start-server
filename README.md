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

# install strapi

npx create-strapi-app app1

or 

npm install strapi@latest -g

or 

npm install -g create-strapi-app

create-strapi-app app1

Strapi cli

https://strapi.io/documentation/3.0.0-beta.x/cli/CLI.html

# install and configure PM2 runtime

npm install pm2@latest -g

cd ~
sudo nano ecosystem.config.js

module.exports = {
  apps: [
    {
      name: 'strapi',
      cwd: '/root/app1',
      script: 'npm',
      args: 'start',
      env: {
        NODE_ENV: 'production',
        DATABASE_HOST: 'localhost', // database endpoint
        DATABASE_PORT: '3306',
        DATABASE_NAME: 'strapi1', // DB name
        DATABASE_USERNAME: 'your-name', // your username for mysql
        DATABASE_PASSWORD: 'password', // your password for         
        DATABASE_USERNAME: 'your-name', // your username for mysql
      },
    },
  ],
};

cd ~

pm2 start ecosystem.config.js

pm2 startup systemd or pm2 unstartup systemd if is already started

pm2 save


# install nginx
https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-18-04
cd ~

sudo apt-get install nginx

sudo ufw app list

sudo ufw status

