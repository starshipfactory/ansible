Ansible Scripts for Infrastructure at SF
========================================
 
This ansible repo currently defines the installation of the various machines in the starship factory. 

Usage:
------
Decrypt the ansible variable file with ansible-vault:
 ansible-vault

To deploy everywhere and everything: 
 ansible-playbook -i inventory site.yml -u root

There are tags for all the roles defined: 
 - ssh_key 
 - info_pi  

To use the playbook with the role only: 
 ansible-playbook -i inventory site.yml -u root -t ssh_key


Role Description:
-----------------
* ssh_key: Deploy ssh_keys of sf members to root account of devices. keys are defined in the ssh_keys variable in group_vars/all.

* info_pi: install info screen for advert screen to the outside
* unattended_upgrades: configure unattended upgrades to install security upgrades automatically.  
