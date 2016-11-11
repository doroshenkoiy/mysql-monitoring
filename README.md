# Mysql/Percona/Mariadb monitoring
# Tested on Debian 8.6, Zabbix 3.2, Percona 5.6

# Trying to start, but now it doesn't working. :(

## Description

Yet another fork of module for mysql monitoring.

## Requirements

- Credentials in /etc/zabbix/zabbix_agentd.d/.my.cnf

## Installing
- Create user for monitoring, e.g.
```
GRANT PROCESS, REPLICATION CLIENT ON *.* TO ‘zabbix’@’localhost’
```
- Put mm.sh into /etc/zabbix/zabbix_agentd.d/ folder
- Run 
```
chmod +x /etc/zabbix/zabbix_agentd.d/mm.sh
```
- Put mm.conf into /etc/zabbix/zabbix_agentd.d/
- Import template to zabbix - mm.xml
- Apply “Template App Mysql Monitoring” template to host
