# AWS EC2 Ubuntu – Direct Root Login Using SSH and Password Authentication

## 📌 Project Title

**Configuring Direct Root User Login on an AWS EC2 Ubuntu Server Using SSH and Password Authentication**

---

## 📖 Project Overview

This project demonstrates the process of connecting to an Ubuntu-based Amazon EC2 instance through SSH using MobaXterm and configuring the server to allow direct login as the `root` user using a password.

By default, an Ubuntu EC2 instance is normally accessed using the `ubuntu` user and an SSH private key (`.pem`). Administrative operations can then be performed using `sudo`.

In this practical task, the SSH configuration of the Ubuntu server was modified so that the `root` account could be accessed directly through SSH using a password.

The complete process includes:

1. Launching an Ubuntu EC2 instance.
2. Connecting to the EC2 instance using MobaXterm.
3. Logging in initially as the `ubuntu` user.
4. Switching to the root shell for configuration.
5. Setting a password for the root account.
6. Editing the OpenSSH server configuration.
7. Enabling root SSH login.
8. Enabling password authentication.
9. Validating the SSH configuration.
10. Restarting the SSH service.
11. Creating a new MobaXterm SSH session.
12. Logging in directly as the `root` user using the configured password.
13. Verifying successful root access.

---

# 🎯 Objectives

The main objectives of this practical task are:

- To understand AWS EC2 instance access.
- To understand SSH-based remote administration.
- To understand the default Ubuntu EC2 login process.
- To understand Linux root-user privileges.
- To configure the OpenSSH server.
- To understand SSH authentication methods.
- To configure password-based SSH authentication.
- To enable direct root login for a controlled lab environment.
- To verify root access using MobaXterm.
- To document the complete procedure using screenshots.

---

# ☁️ AWS EC2 Environment

The server used in this practical task is an Amazon EC2 instance running Ubuntu Linux.

### Server Details

| Parameter | Value |
|---|---|
| Cloud Platform | Amazon Web Services |
| Service | Amazon EC2 |
| Operating System | Ubuntu 26.04 LTS |
| Architecture | x86_64 |
| Protocol | SSH |
| SSH Port | 22 |
| Initial User | ubuntu |
| Target User | root |
| SSH Client | MobaXterm |
| Authentication | SSH Key + Password |
| Server Type | EC2 Virtual Machine |

---

# 🧰 Tools and Technologies Used

## 1. Amazon Web Services (AWS)

Amazon EC2 was used to create and run the Ubuntu virtual server.

EC2 provides a virtual machine in the AWS cloud that can be remotely accessed using SSH.

---

## 2. Ubuntu Linux

Ubuntu was used as the operating system of the EC2 instance.

The server provides a Linux command-line environment where system administration and SSH configuration can be performed.

---

## 3. MobaXterm

MobaXterm was used as the SSH client from the Windows system.

It provides:

- SSH terminal
- SFTP browser
- Session management
- Private-key authentication
- Remote server access
- File transfer capabilities

---

## 4. OpenSSH

OpenSSH provides the SSH server functionality on Ubuntu.

The SSH server configuration is mainly controlled through:

```text
/etc/ssh/sshd_config
