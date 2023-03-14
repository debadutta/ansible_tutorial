# ansible_tutorial

https://www.youtube.com/watch?v=JJ-aoyydfVU&list=PLT98CRl2KxKEUHie1m24-wkyHpEsa4Y70&index=8

This is my awesome ansible repository

Some useful ansible commands:
ansible all -m ping
ansible all --list-hosts
ansible all -m gather_facts
ansible all -m gather_facts --limit 192.168.1.63

Setting firewall after installing webserver on Ubuntu and CentOS

apache2 ubuntu:
sudo iptables -I INPUT 6 -m state --state NEW -p tcp --dport 80 -j ACCEPT
sudo netfilter-persistent save

HTTPD CentOS:
sudo iptables -I INPUT 6 -m state --state NEW -p tcp --dport 80 -j ACCEPT
sudo systemctl restart httpd
    
    Can try this as well for CentOS : sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT
    Learn linux provides this: sudo firewall-cmd --add-port=80/tcp



