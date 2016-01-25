# NCDevOps

This repository contains the script for deploying the infrastructure.

There are 1 playbook, 2 Dockerfiles, config files and empty folders for code in the repo.


If you launch create_containers.yml playbook

```
ansible-playbook create_containers.yml -i hosts
```

you will get the infrastructure which consists of the five containers (not really):

- Nginx balancer (build from Nginx Docker image)
- NodeJS application server #1 (build from Ubuntu Docker image)
- NodeJS application server #2 (build from Ubuntu Docker image)
- Container consists code which mount from the Host (Ubuntu Docker image)
- Mysql container (MySql Docker image)


but if you want to deploy, update, rollback code,  you must have Jenkins with my Items.