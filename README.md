# Simple-Monitoring-Services
A simple script to monitoring service Linux. We created it to help user check service every time when log-in server. This script will help sysadmin vs DevOps to know service running or down.

![alt text](https://i.ibb.co/D1grpQ9/simpel-script.png)

## Installion Script
This script tested and worked on Centos. First, you need to make sure that curl has been installed on your server. After that, you can run this simple command
```
curl -O https://raw.githubusercontent.com/bayuadinh/Simple-Monitoring-Services/master/myservice && chmod +x myservice && mv myservice /usr/bin && echo "myservice all" >> /root/.bashrc
```

## Using Script
### Adding Service
To monitor services, you must first add services you want to monitor. To add, you can simply run the following command
```
myservice add (your-service)
ex
myservice add nginx
```
All service will be add into this location /opt/statuslog/monitor/dataService. 

### Delete Service
You can simple delete service too with following command
```
myservice del (your-service)
ex
myservice del nginx
```

### Check All Service
After adding service, you can simple running this following command
```
myservice all
```

### Check Singgle Service
You can also check the singgle service by using the following command
```
myservice (your-service)
ex
myservice nginx
```