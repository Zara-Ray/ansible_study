# Ansible Study

## Ansible Playbook for Server Configuration and Web Server Deployment using Multiple Roles

### Objective

This Ansible playbook aims to configure and manage three servers: two Ubuntu servers (one functioning as the host server and the other as a web server) and one CentOS server. The playbook is structured with a focus on role-based task grouping to enhance organization and management. The roles encompassed within the playbook are:

- **Script Runner Role**: Executes a bash script or custom commands on the servers as needed.

- **Apache Role**: Installs and configures Apache web server on the Ubuntu servers. Starts the Apache service and deploys web applications or static files.

- **Nginx Role**: Installs and configures Nginx web server on the CentOS server. Starts the Nginx service and deploys web applications or static files.

- **Terraform Role**: Installs Terraform on the host server and manages infrastructure deployments using Terraform.

- **Docker Role**: Installs Docker on all servers and manages containers and containerized applications.


### Playbook Execution

The playbook was executed as a unified playbook with the following structure for roles:

```yaml
---
- hosts: all
  become: true
  gather_facts: true

  tasks:
  ...

  roles:
    - script-runner
    - apache
    - nginx
    - terraform
    - docker
  ...

```

### Conclusion

Through the utilization of this Ansible playbook, the servers were efficiently configured and managed using distinct roles. The **script-runner** role successfully executed bash scripts or custom commands, while the **apache** role effectively installed and configured the Apache web server.

<img src="images/apache_installed_on_host_server.png" width="500"> <img src="images/hosted_page_on_host_server.png" width="500">

Similarly, the **nginx** role proficiently handled the installation and configuration of the Nginx web server.

<img src="images/apache_installed_on_server.png" width="500"> <img src="images/hosted_page_on_server.png" width="500">

Furthermore, the **terraform** and **docker** roles played vital roles in facilitating infrastructure management and containerization, respectively.

<img src="images/apache_installed_on_workserver.png" width="500"> <img src="images/hosted_page_on_workserver.png" width="500">

The collaborative implementation of these roles ensured streamlined server operations and comprehensive system administration.

The accompanying images provide a comprehensive visual representation of the various stages and processes involved in the server configuration and management workflow. These images showcase essential steps ranging from initial setup and connectivity to GitHub, user and server creation, and playbook executions.

The images cover a wide range of activities, including:

- Cloning Git Repositories on Servers via the Host

  <img src="images/cloning_git_repo_on_servers_via_host.png" width="500">

- Creation of Servers

  <img src="images/created_servers.png" width="500">

- User Creation

  <img src="images/creating_user.png" width="500">

- Hosting Pages via Apache

  <img src="images/hosting_page_via_apache.png" width="500">

- Execution

 of Playbook Apache Role

  <img src="images/playbook_apache_role.png" width="500">

- Execution of Playbook Docker Role

  <img src="images/playbook_docker_role.png" width="500">

- Execution of Playbook Nginx Role

  <img src="images/playbook_nginx_role.png" width="500">

- Visualization of Playbook Roles

  <img src="images/playbook_roles.png" width="500">

- Playbook Execution with User

  <img src="images/playbook_run_with_user.png" width="500">

- Execution of Playbook Terraform Role

  <img src="images/playbook_terraform_role.png" width="500">

- Running Scripts with Playbook

  <img src="images/running_script_with_playbook.png" width="500">

- Successful SSH Sign-In

  <img src="images/successful_SSH_sign_in.png" width="500">

- Testing Server Connectivity

  <img src="images/testing_server_connectivity.png" width="500">

- User Confirmation

  <img src="images/user_confirmed.png" width="500">

- User Interface

  <img src="images/user_interface.png" width="500">

- User Sign-In on Slave Servers

  <img src="images/user_on_slave_server_sign_in.png" width="500">

These images serve as valuable references and insights into the diverse processes involved in server configuration and management, enabling effective understanding and implementation of the outlined procedures.
