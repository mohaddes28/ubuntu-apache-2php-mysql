# Install apache-2php-mysql on ubuntu

## update php version
```
sudo update-alternatives --config php
```
### Install Apache 2 and releted 
```
sudo apt update
```
```
sudo apt install apache2 -y
```
```
sudo ufw allow 'Apache'
```
```
sudo ufw status
```
```
sudo systemctl status apache2
```
```
sudo service apache2 status
``` 
```
sudo service apache2 start
```
```
sudo service apache2 stop
```
```
sudo service apache2 restart
```

## Install Php
### Add php Repository
```
sudo apt update
```
```
sudo apt install -y software-properties-common
```
```
sudo add-apt-repository ppa:ondrej/php
```
```
sudo apt update
```
### Install Php7.4
```
sudo apt install -y php7.4 php7.4-cli php7.4-common php7.4-mbstring php7.4-xml php7.4-curl php7.4-mysql php7.4-zip php7.4-gd php7.4-bcmath php7.4-soap php7.4-intl php7.4-readline php7.4-opcache
```
### Install PHP 8.3 and Common Extensions
```
sudo apt install -y php8.3 php8.3-cli php8.3-common php8.3-mbstring php8.3-xml php8.3-curl php8.3-mysql php8.3-zip php8.3-gd php8.3-bcmath php8.3-soap php8.3-intl php8.3-readline php8.3-opcache
```
### (Optional) Install PHP 7.4 for Apache
#### 7.4
```
sudo apt install -y libapache2-mod-php7.4
```
#### 8.3
```
sudo apt install -y libapache2-mod-php8.3
```
### disable and enable php modules for apache i'ts important
```
sudo a2dismod php*     # disable other PHP versions if needed
```

```
sudo a2dismod php7.4
```
```
sudo a2enmod php8.3
```
```
sudo a2enmod php7.4
```
```
sudo systemctl restart apache2
```
or 
```
sudo service apache2 restart
```


