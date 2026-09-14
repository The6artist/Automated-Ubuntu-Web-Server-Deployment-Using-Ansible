# Ansible Web Server Automation In The AWS EC2 Instance 

A beginner-friendly Ansible project that automates the configuration of an Ubuntu web server.

The project prepares the server, installs Nginx, configures Nginx, deploys a static website from a `.tar.gz` archive, configures an SSH public key, and supports role-based execution using Ansible tags.

---

## Project Objective

The goal of this project is to understand the fundamentals of Ansible by automating a simple web server.

Instead of manually performing tasks such as:

- Installing packages
- Installing Nginx
- Configuring Nginx
- Copying website files
- Extracting application files
- Configuring SSH keys

Ansible performs these tasks automatically.

---

## Architecture

For this learning project, Ansible runs directly inside the Ubuntu EC2 instance.

```text

Ubuntu EC2
│
└── Ansible Control Node
    │
    └── localhost
        │
        ├── base role
        │   ├── Update packages
        │   ├── Install curl
        │   ├── Install utilities
        │   └── Install fail2ban
        │
        ├── nginx role
        │   ├── Install Nginx
        │   ├── Configure Nginx
        │   └── Start Nginx
        │
        ├── app role
        │   ├── Copy tarball
        │   └── Extract website
        │
        └── ssh role
            └── Add public SSH key
