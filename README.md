# Ansible Laravel Deployment

This Ansible playbook allows you to deploy Laravel applications with a single command.

## Prerequisites

Ensure that Ansible is installed on the machine where the playbook will be run.

## Configuration

Configure the playbook according to your requirements by setting the following role variables:

- `github_repo`: The Git repository of your Laravel project.
- `hostname`: The domain of your project. Make sure that the domain's DNS is already pointed to the IP address of your server, as this is required by Certbot to issue an SSL certificate.
- `project_name`: The name of your project. This will be used to clone your repository to `/var/www/html/{project_name}`.
- `php_version`: The PHP version for your Laravel project. The default version is 8.1.
- `email_address`: Your email address, needed for Certbot notifications and recovery purposes.

## Usage

Here's an example of how to use this playbook:

```yaml
- hosts: local
  become: yes
  roles:
      - ./Ansible_laravel_deoployment
  vars: 
    github_repo: your_github_repo_url
    hostname: your_domain.com
    project_name: your_project_name
    php_version: 8.1
    email_address: your_email@domain.com
```

Features
------------
- [x] Installs Nginx with proper configurations
- [x] certbot and SSL 
