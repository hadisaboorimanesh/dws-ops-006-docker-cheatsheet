# dws-ops-006-docker-cheatsheet

[@dwsclass](https://github.com/dwsclass) dws-ops-006-docker-cheatsheet

create image for My Project

***From base image***
```
 
 1 - From python:slim

```
***define workdir*** 
```
 2 - WORKDIR /opt/app
```
***Define expose Port***
```
 3 - expose 8080
 ```
 ***Define Env***
 ```
 4 - ENV SKOB_AUTHZ_BIND_ADDRESS=0.0.0.0
     ENV SKOB_AUTHZ_NUM_WORKER=4
 ```
 ***install requirement  package 
 ```
 5 - COPY requirments.txt .
     RUN pip install -r requirments.txt
 ```
 ***Copy  My Project***
 ```
 6 - COPY . .
 ```
 ***define User***
 ```
 7 - RUN useradd -M -d /opt/app authz
     USER authz
 ```
 ***execute command ******
 ```
 8 - CMD ./start
 ```

 
     



***RUN***

```
 
 1 - ansible-playbook -i inventory docker.yaml

```
