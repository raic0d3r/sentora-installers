Sentora Installers (Non Official ModiFied by RaiC0d3r)
==================

Welcome to the Sentora Installation Script Git repository, this provides a central place to store, version and distribute Sentora installer and upgrade scripts from.

## How to install Sentora ##

Our installation script currently support the following operating systems/distributions:

* Debian 8 and 9 and 10
  
 
To install Please use the following command:

```
apt-get update 
apt-get upgrade
sudo apt-get install ca-certificates wget nano dbconfig-common sqlite3 postfix dovecot-imapd dovecot-lmtpd dovecot-pop3d dovecot-sqlite curl sudo
wget http://repo.mysql.com/mysql-apt-config_0.8.13-1_all.deb
sudo dpkg -i mysql-apt-config_0.8.13-1_all.deb
bash <(curl -L -Ss https://raw.githubusercontent.com/raic0d3r/sentora-installers/master/sentora_install.sh)
```
Please note that the MASTER branch installer above is ONLY recommended for developers and project staff!


  
#### Uninstaller scripts ####

Uninstaller scripts, much like the Upgrade scripts are not recommended for use at present but we also need to make it clear that although they remove most of the packages installed by the Sentora Installation scripts they will not leave your OS in his initial state given the large amount of customisations that our installation scripts make.

* * *
## ALL INFORMATION BELOW MAY BE INACCURATE OR INCOMPLETE ##
* * *


Folders mounted to /root/sentora/{install,uninstall,upgrade}

## Official maintainers ##


Sentora important files paths and OS specificities

```
File or directory	 	Debian
Sentora passwords file	 	/root/passwords.txt
Sentora config files	 	/etc/sentora/configs/
Sentora config - apache config file	 	/etc/sentora/configs/apache/httpd.conf
Sentora config - virtual host file	 	/etc/sentora/configs/apache/httpd-vhosts.conf
Sentora config - FTP config file	 	/etc/sentora/configs/proftpd/proftpd-mysql.conf
Sentora panel files	 	/etc/sentora/panel/
Sentora panel static pages	 	/etc/sentora/panel/etc/static/
Sentora panel themes	 	/etc/sentora/panel/etc/styles/
Sentora log files	 	/var/sentora/logs/
Sentora users websites	 	/var/sentora/hostdata/[Sentora-login]/public_html/[domain_tld]
Sentora email data	 	/var/sentora/vmail/[domain.tld]
 	 	 	 
Apache config file	 	/etc/apache2/httpd.conf	/etc/httpd/conf/httpd.conf
Apache log files	 	/var/log/apache2/error.log	/var/log/httpd/error.log
 	 	 	 
Php.ini	 	 /etc/php5/apache2/php.ini	/etc/php.ini
 	 	 	 
Mysql config file	 	/etc/mysql/my.cnf	/etc/my.cnf
Mysql log file	 	/var/log/mysql/error.log	/var/log/mysqld.log
 
```

Other infos	Debian

```
Apache user:group	www-data:www-data	apache:apache

```
How to restart apache ?	

```
service apache2 restart	
service httpd restart

```
Run Sentora daemon	
```
sudo /usr/bin/php -q /etc/sentora/panel/bin/daemon.php

``` 	 	 

If you have any queries regarding the above rules please feel free to contact me at: [raic0d3r@gmail.com](mailto:raic0d3r@gmail.com).
