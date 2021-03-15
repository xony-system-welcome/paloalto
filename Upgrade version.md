Upgrade version capture\
https://docs.google.com/document/d/1JU9B1KeRyPWmjz-_YwaGqcOKTRwjBCviEKE6kggcSc4/edit?usp=sharing

---
###### Basic Command\
```> Ping host {IP}```
---
##### 1.Basic Setup and check about IP and version

1.1. View device version\
```> debug swm list```

1.2. View Device IP\
```> show interface management```

1.3. List PAN-OS software\
```> request system software info```

1.4. Shutdown device\
```> request shutdown system```

1.5. Run configuration mode\
```> configure```

1.6. Change the management ip\
```# set deviceconfig system ip-address x.x.x.x netmask x.x.x.x default-gateway x.x.x.x```

1.7. Commit the changes\
```# commit```

##### 2.Backup configuration file
2.1. Entering Configuration mode\
```> configure```

2.2. Configuration file save\
```# save config to 2021-03-15_configuration.xml```

2.3. Exit\
```# exit```

2.4. Export configuration file\
```# scp export configuration from 2021-03-15_configuration.xml to username@scpserver/PanConfigs```


##### 3.Install and Download PAN-OS file
3.1. List PAN-OS software again\
```> request system software info```

3.2. List and check PAN-OS\
```> request system software check```

If have't list upgrade version we can upload folder on GUI.\

3.3. Download PAN-OS version\
 ```> request system software download version x.x.x```
 
3.4. Install PAN-OS version\
```> request system software install version x.x.x```

3.5. Finish install Restart system\
```> request restart system```

3.6 Check version\
```> debug swm info```

If have error 'version xxx of the Content Database is required for the upgrade.' \
Need update Content Database version\

3.7 Check content database version\
```> show system info```

3.8 Download latest content database version\
```> request content upgrade download latest```

3.9 Install latest content database version\
```> request content upgrade install version latest```

3.10. Check content database version\
```> show system info```

3.11. Install PAN-OS version\
```> request system software install version x.x.x```

3.12. Finish install Restart system\
```> request restart system```

3.13. Check version\
```> debug swm info```
 
