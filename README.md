# dws-ops-006-docker-cheatsheet

[@dwsclass](https://github.com/dwsclass) dws-ops-006-docker-cheatsheet

Install docker with ansible.

**this playbook consist installing docker with ansible on Ubuntu**

for installing **docker** refer this [Link](https://docs.docker.com/engine/install/ubuntu/)

***From base image***
```
 
 1 - From python:slim

```
***define workdir*** 
```
 2 - WORKDIR /opt/app
```


***RUN***

```
 
 1 - ansible-playbook -i inventory docker.yaml

```
