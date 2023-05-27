# ansible_study

## Ansible Playbook for Server Configuration and Web Server Deployment using Multiple Roles

### Objective

This Ansible playbook aims to configure and manage three servers: two Ubuntu servers (one functioning as the host server and the other as a web server) and one CentOS server. The playbook is structured with a focus on role-based task grouping to enhance organization and management. The roles encompassed within the playbook are:

- **Script Runner Role**: Executes a bash script or custom commands on the servers as needed.
  ![Script Runner Role](/script_runner_role.png)

- **Apache Role**: Installs and configures Apache web server on the Ubuntu servers. Starts the Apache service and deploys web applications or static files.
  ![Apache Role](/apache_role.png)

- **Nginx Role**: Installs and configures Nginx web server on the CentOS server. Starts the Nginx service and deploys web applications or static files.
  ![Nginx Role](./images/nginx_role.png)

- **Terraform Role**: Installs Terraform on the host server and manages infrastructure deployments using Terraform.
  ![Terraform Role](./images/terraform_role.png)

- **Docker Role**: Installs Docker on all servers and manages containers and containerized applications.
  ![Docker Role](./docker_role.png)

### Playbook Execution

The playbook was executed as a unified playbook with the following structure for roles:

```yaml
- name: Server Configuration, Web Server Deployment, and Multiple Roles
  hosts: all
  roles:
    - script-runner
    - apache
    - nginx
    - terraform
    - docker
```

### Conclusion

Through the utilization of this Ansible playbook, the servers were efficiently configured and managed using distinct roles. The **script-runner** role successfully executed bash scripts or custom commands, while the **apache** role effectively installed and configured the Apache web server.
![Apache Installed on Host Server](images/apache_installed_on_host_server.png) ![Hosted Page on Host Server](images/hosted_page_on_host_server.png)

Similarly, the **nginx** role proficiently handled the installation and configuration of the Nginx web server.
![Apache Installed on Server](images/apache_installed_on_server.png) ![Hosted Page on Server](images/hosted_page_on_server.png)

Furthermore, the **terraform** and **docker** roles played vital roles in facilitating infrastructure management and containerization, respectively.
![Apache Installed on Work Server](images/apache_installed_on_workserver.png) ![Hosted Page on Work Server](images/hosted_page_on_workserver.png)

The collaborative implementation of these roles ensured streamlined server operations and comprehensive system administration.

The accompanying images provide a comprehensive visual representation of the various stages and processes involved in the server configuration and management workflow. These images showcase essential steps ranging from initial setup and connectivity to GitHub, user and server creation, and playbook executions.

The images cover a wide range of activities, including:

- Cloning Git Repositories on Servers via the Host
  ![Cloning Git Repo on Servers via Host](images/cloning_git_repo_on_servers_via_host.png)

- Creation of Servers
  ![Created Servers](images/created_servers.png)

- User Creation
  ![Creating User](images/creating_user.png)

- Hosting Pages via Apache
  ![Hosting Page via Apache](images/hosting_page_via_apache.png)

- Execution of Playbook Apache Role
  ![Playbook Apache Role](images/playbook_apache_role.png)

- Execution of Playbook Docker Role
  ![Playbook Docker Role](images/playbook_docker_role.png)

- Execution of Playbook Nginx Role
  ![Playbook Nginx Role](images/playbook_nginx_role.png)

- Visualization of Playbook Roles
  ![Playbook Roles](images/playbook_roles.png)

- Playbook Execution with User
  ![Playbook Run with User](images/playbook_run_with_user.png)

- Execution of Playbook Terraform Role
  ![Playbook Terraform Role](images/playbook_terraform_role.png)

- Running Scripts with Playbook
  ![Running Script with Playbook](images/running_script_with_playbook.png)

- Successful SSH Sign-In
  ![Successful SSH Sign In](images/successful_SSH_sign_in.png)

- Testing Server Connectivity
  ![Testing Server Connectivity](images/testing_server_connectivity.png)

- User Confirmation
  ![User Confirmed](images/user_confirmed.png)

- User Interface
  ![User Interface](images/user_interface.png)

- User Sign-In on Work Server
  ![User on Slave Server Sign In](images/user_on_slave_server_sign_in.png)

These images serve as valuable references and insights into the diverse processes involved in server configuration and management, enabling effective understanding and implementation of the outlined procedures.
