Ansible_laravel_deoployment
=========

Deploy Laravel with one command

Requirements
------------

Ansible must be installed.

Role Variables
--------------

    github_repo: your Git repo
    hostname: Project domain, needs an IP address pointing to your domain. Certbot needs that to issue a certificate.
    project_name: Project name, Your repo will be cloned to /var/www/html/{poject_name}.
    php_version: 8.1
    email_address: your Email Address.



Example Playbook
----------------

Including an example of how to use the role :

- hosts: local
  become: yes
  roles:
      - /root/Ansible_laravel_deoployment
  vars: 
    github_repo: 
    hostname: 
    project_name: 
    php_version: 8.1
    email_address:


Features
------------
- [x] Installs Nginx with proper configurations
- [x] certbot and SSL 
