-----------------------------------------------
#### ansible-playbooks Git, Jenkins
  my test works for learning ansible
  
##### Requirements:
  - Anible version 2.12.1
 
  - access via ssh to target host
 
  - update hosts file and add your settings like this
    
  [name_group]
  
  Servername ansible_host=your_hostname_ip ansible_user=your_username ansible_ssh_private_key_file=/home/ubuntu/.ssh/your_ssh_key
  
  - update ansible.cfg like this (need indicate your inventory file, and ignore host_key_checking)
 
  [defaults]
  
  host_key_checking = false
  
  inventory         = ./hosts.txt
 
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
  - update hosts file and add your settings like this
    
  [name_group]
  
  Servername ansible_host=your_hostname_ip ansible_user=your_username ansible_ssh_private_key_file=/home/ubuntu/.ssh/your_ssh_key
 
 - update ansible.cfg like this (need indicate your inventory file, and ignore host_key_checking)
  
  [defaults]
  
  host_key_checking = false
  
  inventory         = ./hosts.txt
  
##### Settings 
  in the playbook lamp.yml (to increase security use ansible vault)
  
  #MySQL settings
  
  mysql_root_password: "QV=5bVX2"   - the password for the MySQL root account.
  
  mysql_db: "wordpress"             - the name for the MySQL database.
  
  mysql_user: "wordpressuser"       - the name for the MySQL account.
  
  mysql_password: "7k0xAS*x"        - the password for the MySQL wordpressuser account.
  
  #HTTP settings:
  
  http_host: "my-domain"
  
  http_conf: "my-domain.conf"
  
  http_port: "80"

##### configure templates
  in the files directory u can check jinja templates if u need add some changes

##### Run the Playbook
  cd to your ansible directory and use command
  
  ansible-playbook lamp.yml -K
