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
https://raw.githubusercontent.com/Aureliolo/Jelastic-Zabbix-Agent/master/main.jps
```

Or copy the content of main.jps into the import window.


# Usage
When installing the addon you have 3 options to configure:

<img src="https://github.com/Aureliolo/Jelastic-Zabbix-Agent/raw/master/images/configuration.png" width="520">

All 3 get set in /etc/zabbix/zabbix_agentd.conf

Server IP gets set as the config options <code>ServerActive</code> and <code>Server</code>\
Remote Command execution either sets <code>EnableRemoteCommands=1</code> or <code>DenyKey=system.run[*]</code> \
Remote Logging is only available if Remote Command is activated and sets either <code>LogRemoteCommands=1</code> or <code>LogRemoteCommands=0</code>


Once the Addon is installed there are 2 available buttons:

<img src="https://github.com/Aureliolo/Jelastic-Zabbix-Agent/raw/master/images/interface.png" width="520">

Update will update the agent to newest version.

Configurate allows you to reset the 3 options to new values if needed.
