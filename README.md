-----------------------------------------------
#### ansible-playbooks Git, Jenkins
  
 my test works for learning Ansible
  
##### Requirements:
  
    - Anible version 2.12.1
 
  - access via ssh to target host

##### Pre-configure:
  
  - update hosts file and add your settings like this
    
  ```[name_group]```
  
  ```Servername ansible_host=your_hostname_ip ansible_user=your_username ansible_ssh_private_key_file=/home/ubuntu/.ssh/your_ssh_key```
  
##### Run the Playbook
 
  cd to your ansible directory and use command as u need
  
  ansible-playbook gitplaybook.yml -K
  
  ansible-playbook jenkins_install_playbook.yml -K

------------------------------------------------

#### LAMP with WP on Ubuntu 20.04

  Linux, Apache, MySQL and PHP with WordPress
  
  cp folder LAMP to your ansible directory

##### Requirements:
   
  - Anible version 2.12.1
  - access via ssh to target host
 
##### Pre-configure:
  
 - update hosts file and add your settings like as described above in the text
    
##### Run the Playbook

  cd to your ansible directory and use command
  
  ansible-playbook lamp.yml -K
  
-----------------------------------------------
