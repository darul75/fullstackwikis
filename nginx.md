# Install / Config

* Edit /usr/local/etc/nginx/nginx.conf

* Check user

Replace this fucking line
```
#user  nobody;
```
by
```
user  username staff;
```

* Add Virtual Host:

```
    #keepalive_timeout  0;
    keepalive_timeout  65;

    #gzip  on;

    ##
    # Virtual Host Configs
    ##

    include /usr/local/nginx/sites-enabled/*;	
```
* Create sites

```
cd /usr/local/nginx
mkdir sites-available
mkdir sites-enabled
```

* Copy these 2 files from link below into `sites-available`

https://github.com/ganmor/Beedeez/tree/master/src/config/nginx

* Update mobile-client change directory match local config

Mobile Client config is a virtual host that serve client files on port 4000.
You need to chnage the root directory to match with your local install

Replace path in (l.10):

```
root  /{BasePathofYourProject}/src/client/html5-core/app/;
```

* Make symbolic link from site enabled to site-available

From the site-enabled directory use :

```
ln -s ../sites-available/beedeez-proxy beedeez-proxy
ln -s  ../sites-available/mobile-client mobile-client
```

## Common executable directory
```
sudo /usr/local/bin/nginx
```

## Kill nginx brute force
```
ps -ax | grep nginx
kill pid
```

## Reload conf
```
sudo /usr/local/bin/nginx -s reload
```
