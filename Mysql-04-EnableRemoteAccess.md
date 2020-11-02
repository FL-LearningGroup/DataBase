## Overview
The mysql default disable remote access.

### Enable root remote access
+ Step01: Edit configuration bind-address
  - sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf (ubuntu)
  - Change parameter **bind-address=127.0.0.1 --> 0.0.0.0**
  - sudo service mysql restart
+ Step02: grant remote access privilege to root
  - grant all privileges on *.* to 'root'@'%' identified by 'password' with grant option;
  - flush privileges;
