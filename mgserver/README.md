# Ansible playbooks for MGServer

This playbooks setup and deploy applications necessary to operate
MGServer on Ubuntu 12.04 64-bit server.

## Execute playbooks

**NOTE:** Ansible is required on the local machine to execute
playbooks.

Use the following command to execute this playbooks.

    $ ansible-playbook setup.yml --private-key=<private_key> -i hosts
    $ ansible-playbook deploy.yml --private-key=<private_key> -i hosts

`<private_key>` is the path to the private key to ssh into the
server. For EC2 servers, this will be a `*.pem` file.

`hosts` is the inventory file, which contains list of servers that
this playbooks will work with.

## What are installed/configured

 * Nginx
 * uWSGI
 * MongoDB
 * Pip
 * virtualenv
 * [MGServer Web API][]

## References

 * [Flask/WSGI Application Deployment with Ubuntu, Ansible, Nginx, Supervisor and uWSGI][1]
 * [Ansible Documentation][2]

[MGServer Web API]: https://github.com/Avamagic/mgserver-web-api
[1]: http://mattupstate.github.com/python/devops/2012/08/07/flask-wsgi-application-deployment-with-ubuntu-ansible-nginx-supervisor-and-uwsgi.html
[2]: http://ansible.cc/docs/
