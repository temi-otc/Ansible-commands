# Ansible-commands
#Commands for creating playbook and executing it in Ansible

ssh-keygen - to generate pub and private keys

ssh-copy-id -i id_rsa.pub (private ip of target vm) - copy  pub key to the target nodes

Web01 ansible_host=10.0.2.5 ansible_user=temi
Db01 ansible_host=10.0.3.5 ansible_user=temi

ansible Web01 -i inventory.hosts -m ping - Pinging the target nodes from the controller/master node and targeting either a "web01" user or a group namd "web01"

ansible all -i inventory.hosts -m ping - Pinging all nodes from the controller/master node

Ansible-playbook play.yml -I inventory.hosts - commands for running the playbook

Ansible-playbook ansible/play.yml ansible/inventory.hosts - commands for running the playbook(provided the files are in different directories)
