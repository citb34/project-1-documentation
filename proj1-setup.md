### Documentation to setup your application.

#### Assuming the following architecture , Doc has been made.

![image](https://user-images.githubusercontent.com/29029753/50553231-9daf1380-0cc8-11e9-9281-1ff2f3685d04.png)


#### 1. Install and Start Web Server.

```
$ sudo yum install httpd -y
$ sudo systemctl enable httpd
$ sudo systemctl start httpd
```

##### Configure Web Server.
```
$ sudo cat /etc/httpd/conf.d/studentapp.conf
ProxyPass "/student"  "http://localhost:8080/student"
ProxyPassReverse "/student"  "http://localhost:8080/student"

$ sudo wget https://raw.githubusercontent.com/citb34/project-1-documentation/master/httpd-index.html -O /var/www/html/index.html

$ sudo systemctl restart httpd
```


