# Linux Server Automation Using Ansible

## Project Overview

This project demonstrates how to automate Linux server administration using **Ansible**.

The main objective is to simplify repetitive system administration tasks and manage Linux servers efficiently through Ansible playbooks. Instead of manually configuring each server, Ansible automates common administrative operations remotely over SSH.

This is my first beginner-level Ansible automation project, developed as part of my DevOps learning journey.

## Objectives

- Understand Ansible architecture and how it works.
- Establish SSH connectivity between the control node and managed node.
- Automate common Linux system administration tasks.
- Manage users and groups.
- Install and manage system packages.
- Configure SSH services.
- Manage UFW firewall rules.
- Start, stop, enable, and manage system services.
- Configure file and directory permissions.

## Technologies Used

| Technology | Purpose |
|---|---|
| Ansible | Configuration management and automation |
| Linux | Operating system administration |
| Ubuntu Server | Managed server |
| SSH | Remote server connectivity |
| YAML | Writing Ansible playbooks |
| UFW | Firewall management |

## Architecture

The project follows Ansible's agentless architecture.

- **Control Node:** The machine where Ansible is installed and playbooks are executed.
- **Managed Node:** The remote Linux server configured and managed by Ansible.
- **SSH:** Used for secure communication between the control node and managed node.

## Tasks Automated

### 1. User Management
- Create Linux users.
- Manage user accounts.
- Configure user-related settings.

### 2. Package Management
- Update package repositories.
- Install required system packages.
- Manage installed packages.

### 3. SSH Configuration
- Manage SSH service configuration.
- Ensure the SSH service is running.
- Enable the service at system startup.

### 4. Firewall Management
- Install and configure UFW.
- Manage firewall rules.
- Allow required network traffic.

### 5. Service Management
- Start and stop services.
- Enable services at boot.
- Ensure required services are running.

### 6. File and Directory Permissions
- Manage file ownership.
- Configure directory permissions.
- Maintain appropriate access permissions.

## Prerequisites

Before running this project, ensure you have:

- Ansible installed on the control node.
- A Linux managed server.
- SSH connectivity between both machines.
- A user with appropriate sudo privileges.
- Network connectivity between the machines.

## How to Run the Project

**Step 1: Clone the repository**

```bash
git clone <your-repository-url>
cd linux-server-automation
```

**Step 2: Configure the inventory**

Add your managed server's IP address and SSH user to the Ansible inventory file.

Example:

```ini
[servers]
192.168.1.100 ansible_user=ubuntu
```

Replace the example IP address and username with your managed server details.

**Step 3: Test connectivity**

```bash
ansible all -i inventory.ini -m ping
```

**Step 4: Check playbook syntax**

```bash
ansible-playbook -i inventory.ini playbook.yml --syntax-check
```

**Step 5: Execute the playbook**

```bash
ansible-playbook -i inventory.ini playbook.yml
```

## Learning Outcomes

Through this project, I gained practical experience with:

- Ansible installation and configuration.
- Ansible inventory management.
- SSH-based remote server management.
- YAML syntax and Ansible playbooks.
- Ansible modules for Linux administration.
- Automated package and service management.
- Linux user and permission management.
- Basic firewall configuration.
- Understanding infrastructure automation and configuration management.

## Future Improvements

- Organize playbooks using Ansible roles.
- Introduce Ansible variables and templates.
- Implement handlers for service restarts.
- Improve task reusability and maintainability.
- Automate more advanced server configuration tasks.

## Author

**Sakil Shrestha**

Aspiring DevOps Engineer | Linux | Docker | Ansible | Networking

