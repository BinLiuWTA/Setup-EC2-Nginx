#Install NGINX server in EC2 Ubuntu Instance

Reference: https://www.nginx.com/blog/setting-up-nginx/

In terminal, login to EC2 instance

1, Download the NGINX signing key

`sudo wget http://nginx.org/keys/nginx_signing.key`

2, Add the key

`sudo apt-key add nginx_signing.key`

3, Change directory to /etc/apt

`cd /etc/apt `

4, Open Source.list, append the following at the end

``` 
deb http://nginx.org/packages/ubuntu xenial nginx
deb-src http://nginx.org/packages/ubuntu xenial nginx
```

5, Update the NGINX software

`sudo apt-get update`

6, Install NGINX:

`sudo apt-get install nginx`

7, Type `Y` When prompted

8, `sudo mkdir -p /var/www/myawesomewebsite.com/html`

9, `sudo chown -R $User:$User /var/www/myawesomewebsite.com/html`

10, `sudo chmod -R 755 /var/www`

11, Start NGINX

`sudo service nginx start`

12, Configuration file is under `/etc/nginx/config.d/`


