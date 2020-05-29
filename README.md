# Jelastic-Zabbix-Agent
Installs the Zabbix agents and connects it to your zabbix server


**Only CENTOS based nodes are supported** 
This should be all the nodes where the user has no root rights by default essentially.

To know if your node is supported you can use this command in shell:
```
cat /etc/*release
```
If it says centos then you can install this addon.


# Installation
Simply import this link using the Jelastic JPS Import function:
```
https://raw.githubusercontent.com/panslothda/Jelastic-Zabbix-server/master/main.jps
```

Or copy the content of main.jps into the import window.


# Usage
When installing the addon you have 3 options to configure:

![Interface](images/configuration.png?raw=true)

All 3 get set in /etc/zabbix/zabbix_agentd.conf

Server IP gets set as the config options <code>"ServerActive"</code> and <code>"Server"</code>
Remote Command execution either sets <code>"EnableRemoteCommands=1"</code> or <code>"DenyKey=system.run[*]"</code>
