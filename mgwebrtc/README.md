# Ansible playbooks for webrtc

This playbooks setup and deploy applications necessary to operate
webrtc on Ubuntu 12.04 64-bit server.

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

 * node.js

## References
