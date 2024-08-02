# Virtual Machine Configuration with Vagrant and Ansible

Hi there!

This repository contains a basic configuration for a virtual machine using Vagrant and Ansible.

## Vagrant

- **Provisioning**: Configures the virtual machine (VM) with the following features:
  - **Public Network**: Configures the VM to use a public network for better connectivity.
  - **Synced Folder**: Syncs a `.html` file to the VM, which may be used for Nginx or other purposes.
  - **Ansible Installation**: Installs Ansible on the VM following the official documentation.
  - **Playbook Execution**: Executes an Ansible playbook that is configured to use the specified role.

## Ansible

- **Automated Installation and Configuration**: Uses Ansible for automated setup:
  - **Role Structure**: Implements a role with:
    - **Task File**: Defines tasks for the installation and configuration of Nginx.
    - **Template**: Provides a Jinja2 template for Nginx configuration.
    - **Handler File**: Manages notifications, such as restarting Nginx when configuration changes.
  - **Playbook**: Configures the VM to use the role for installing and configuring Nginx.



