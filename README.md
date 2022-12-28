# Docker ITI

## Lab1

### Problem1

![plot](./Day1/Screenshot%20from%202022-12-28%2013-14-58.png)


```bash
$ sudo docker run hello-world
$ sudo docker ps -a
$ sudo docker start 64d459f955b3
$ sudo docker rm 64d459f955b3
$ sudo docker images
$ sduo docker rmi feb5d9fea6a5
```


### Problem2

![plot](Day1/Screenshot%20from%202022-12-28%2013-16-04.png)


```bash
$ sudo docker run -it ubuntu
$ echo docker
$ touch hello-docker
$ sudo docker stop d3917c73d21d
$ sudo docker rm d3917c73d21d
```
\# all files deleted once I removed the container

```bash
$ sudo docker container prune
```


### Problem3

![plot](./Day1/Screenshot%20from%202022-12-28%2013-16-32.png)


```bash
$ sudo docker volume create vol
$ sudo docker run -it -v vol:/usr/share/nginx/html -p 8085:80 --name nginxCon5 nginx bash
$ cd /usr/share/nginx/html/
$ echo "Remon Louis" >> index.html 
$ service start nginx
$ sudo docker stop faa
$ sudo docker rm faa
$ sudo docker run -it -v vol:/usr/share/nginx/html -p 8088:80 --name nginxCon6 nginx bash
$ service start nginx
```

### Problem4

![plot](./Day1/Screenshot%20from%202022-12-28%2013-16-58.png)


```bash
$ sudo docker run -it -p 8090:80 --name nginxCon8 nginx bash
$ cd /usr/share/nginx/html/
$ toch RemonLouis.html
$ echo "Remon Louis" >> RemonLouis.html 
$ sudo docker images
$ sudo docker commit ed579e1e3144 testimage:version1.0
# Docker file created
$ sudo docker build -t remonlouis_image .
```
### Problem5

![plot](./Day1/Screenshot%20from%202022-12-28%2013-17-31.png)

```Bash
$ sudo docker run --name app-database9 -v mysql_data:/var/lib/mysql -p 3040:3306 -e MYSQL_ROOT_PASSWORD=P4sSw0rd0! -d mysql
```
