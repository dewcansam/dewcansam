# How2 Add A New Virtual Domain Using Port Numbers #

    @author         Christopher L Smith
    @copyright      2019-02-17 04:12:16
    @file           how2_add-new-virt-site.md
    @version        1.1
    @updated        2024-05-28 00:09:06 -5

## OLD CONFIG FILE ##

```config
Listen ${V_PORT}
<VirtualHost *:${V_PORT}>

ServerName ${V_SITE_DOMAIN}
#ServerAlias ${V_ALIAS}
DocumentRoot /var/www/virtWeb/${V_SITE_DOMAIN}
ServerAdmin ${V_USER}@${V_SITE_DOMAN}
#LogLevel info ssl:warn
ErrorLog ${APACHE_LOG_DIR}/${V_SITE_DOMAIN}_error.log
CustomLog ${APACHE_LOG_DIR}/${V_SITE_DOMAIN}_access.log combined
#Include conf-available/serve-cgi-bin.conf
#Options +indexes

</VirtualHost>

# vim: syntax=apache ts=4 sw=4 sts=4 sr noet
```    

## USER VARIABLES ##

```config
${V_ALIAS}
${V_PORT}
${V_USER}
${V_SITE_DOMAIN}
```    

## HOW2 USE USER VARIABLES ##

All user variables are the ones we need to change  
using vim this can be done with the following commands  

```vim
:%s/${V_ALIAS}/newservername/g
:%s/${V_PORT}/newserverport/g
:%s/${V_USER}/user/g
:%s/${V_SITE_DOMAIN}/newserverdomain/g
``` 

## NEW CONFIG FILE ##


## ADD TO SITES-AVAILABLE AND RESTART ##

```bash
$ cd /etc/apache2/sites-enabled
$ sudo cp ../sites-available/8800.conf ../sites-available/8816.conf
$ sudo vi ../sites-available/8816.conf
$ sudo ln -s ../sites-available/8816.conf
$ sudo service apache2 reload
```


```html
//* sample variable pulled from /etc/apache2/envvars */  
//* it would be cool if I could figure out if I could use this */  
```

export APACHE_PID_FILE=/var/run/apache2/apache2$SUFFIX.pid
