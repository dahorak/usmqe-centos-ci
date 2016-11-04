This directory contains Ansible playbooks for getting resources from CentOS CI
and returning them to pool.

Files:
 - *centos-tendrl1.yml* 
   Ansible playbook for getting machines from CentOS CI pool. This file is 
   definition of one cluster. For now there is just one cluster prepared
   for acceptance testing in CentOS CI. This playbook saves file with ssid 
   for cluster(centos-tendrl1 in this case) to file 
   ~tendrl/centos-tendrl1.ssid
   and inventory file for setup Ansible playbooks to file 
   ~tendrl/centos-tendrl1.hosts

 - *centos-inventory.yml*
   Ansible playbook for updating file with ssid and inventory file
   for specified clustername.

 - *centos-teardown.yml*
   Ansible playbook for returning machines back to pool for specified 
   clustername.

All playbooks can be run by command where should be specified empty inventory file,
clustername and path to cico module. Example for updating inventory and ssid files:
```
ansible-playbook -i empty.hosts -e clustername=centos-tendrl1 -M /usr/lib/python2.7/site-packages/cicoclient/ansible/ centos-inventory.yml
```
