# Automation Project with Ansible

## Overview

This repository contains an automation project designed to streamline the deployment process for multiple software packages across three VirtualBox instances using a single command. The goal is to automate the installation of software packages, orchestrating VirtualBox environments to facilitate simultaneous deployment in testing scenarios.

## Features

- **Robust Ansible Playbook:** The project includes a well-structured Ansible playbook that automates the installation of various software packages on VirtualBox instances. The playbook is designed for efficiency and reliability.

- **Orchestration of VirtualBox Environments:** The automation project orchestrates VirtualBox environments, allowing for the simultaneous deployment of software packages across multiple instances. This is particularly useful for testing scenarios where parallel deployment is required.

- **Significant Reduction in Deployment Time:** By implementing efficient automation processes, the project has successfully reduced deployment time, providing a quick and reliable way to deploy software packages.

- **Adaptability:** Regular updates and maintenance of Ansible playbooks ensure adaptability to changes in software configurations. This helps in keeping the automation process up-to-date and compatible with evolving software requirements.

## Getting Started

### Prerequisites

Before running the automation project, ensure you have the following prerequisites:

- VirtualBox installed on your local machine.
- Ansible installed on your local machine.

## Configuration

### Ansible Inventory (`/etc/ansible/hosts`)

The Ansible inventory file `/etc/ansible/hosts` is configured with target hosts and global variables:

```ini
# Target host
[servers]

# ubuntu with SSH key authentication on port 2222. /Server
# centos with SSH key authentication on port 2200. /Rhel
# Uses user "vagrant and ssh key location ~/.ssh/Access-Host.
ubuntu ansible_user=vagrant ansible_port=2222 ansible_ssh_private_key_file=~/.ssh/Access-Host
centos ansible_user=vagrant ansible_port=2200 ansible_ssh_private_key_file=~/.ssh/Access-Host

# Global variables that apply to all hosts defined in this inventory file.
[all:vars]
ansible_python_interpreter=/usr/bin/python3

```

The Ansible inventory file `/etc/hosts` is configured with target hosts and global variables:

```ini
# Configuration under /etc/hosts
127.0.0.1     ubuntu
127.0.0.1     centos
```
![Draft](https://github.com/RajeevThapa/ansible-automation/assets/101322664/d9ae368c-ea33-4530-88f9-8419a650b8b0)

