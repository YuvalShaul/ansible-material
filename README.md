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

## Second example - using a role

- This example does exactly the same, but leaves the main Ansible file (playbook2.yaml) simple and clean.  
- The "heavy lifting" of docker installation is done by the role (called docker_role here).
- I have created the role using this command (that you DONT have to run):
```
ansible-galaxy init docker_role
```
- After all the role folders were created, I could edit the ./docker_role/tasks/main.yml to add the list of task I wanted.
- Running:
  - Create a new ec2 instance
  - update the external IP address in hosts file
  - run:
```
ansible-playbook -i hosts  playbook2.yaml
```

