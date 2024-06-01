# Replikasi Master Slave MySQL 5.7

## Perangkat Percobaan
a. Distro: Ubuntu Server 18.04 LTS <br />
b. MySQL: 5.7 <br />
c. IP Master: 172.16.24.24 <br />
d. IP Slave: 172.16.24.240 

### Konfigurasi Server Database Master:
1. #### Buka file konfigurasi mysql
```nano
  sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a. ubah IP bind-address, isi dengan ip address server database master:
```nano
      bind-address = 172.16.24.24
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; b. hilangkan comment / tambahkan baris:
```vim
      server-id = 1
      log_bin = /var/log/mysql/mysql-bin.log
```



