# ansible-playbooks
my test work for learning ansible

# LAMP with WP on Ubuntu 20.04
Linux, Apache, MySQL and PHP with WordPress

Settings

mysql_root_password: "QV=5bVX2"   - the password for the MySQL root account.
mysql_db: "wordpress"             - the name for the MySQL database.
mysql_user: "wordpressuser"       - the name for the MySQL account.
mysql_password: "7k0xAS*x"        - the password for the MySQL wordpressuser account.

#HTTP settings
http_host: "my-domain"
http_conf: "my-domain.conf"
http_port: "80"

# Run the Playbook
sudo ansible-playbook lamp.yml -K
