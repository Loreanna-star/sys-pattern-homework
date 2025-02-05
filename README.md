# Домашнее задание к занятию "`Система мониторинга Zabbix`" - `Хованская Светлана`


### Задание 1

```
wget https://repo.zabbix.com/zabbix/6.4/ubuntu/pool/main/z/zabbix-release/zabbix-release_latest_6.4+ubuntu22.04_all.deb
dpkg -i zabbix-release_latest_6.4+ubuntu22.04_all.deb
apt update
apt install zabbix-server-pgsql zabbix-frontend-php php8.1-pgsql zabbix-apache-conf zabbix-sql-scripts zabbix-agent
sudo -u postgres createuser --pwprompt zabbix
sudo -u postgres createdb -O zabbix zabbix
zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix
systemctl restart zabbix-server zabbix-agent apache2
systemctl enable zabbix-server zabbix-agent apache2

```
Скриншот-1 к заданию 1:
![Скриншот-1](https://github.com/Loreanna-star/sys-pattern-homework/blob/zabbix_1/img/task1-1.png)
Скриншот-2 к заданию 1:
![Скриншот-1](https://github.com/netology-code/sys-pattern-homework/blob/main/img/img15.png)
Скриншот-3 к заданию 1:
![Скриншот-1](https://github.com/netology-code/sys-pattern-homework/blob/main/img/img15.png)

### Задание 2
