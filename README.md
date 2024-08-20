# ansible-material
Ansible demos and exercises.

## First example - playbook1.yaml
This example installs Docker engine on anaws ec2 instance.
How to run:
- Make sure Ansible is installed on your working host
- Clone this repository
- Run a new ec2-instance using AMI-2 ami
- Make sure it is accessible from the public internet, and port 22 (SSH) is available
- Edit the 'hosts' file you have cloned and change the IP address of the host in the [docker_grp] to the correct IP address.
- Run the Ansible command:
```
ansible-playbook -i hosts  playbook1.yaml
```

