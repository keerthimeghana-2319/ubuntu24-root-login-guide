# AWS EC2 Ubuntu 24.04 – Direct Root SSH Login

## Overview

This project demonstrates how to configure an AWS EC2 instance running Ubuntu 24.04 to allow direct SSH login as the `root` user using password authentication through MobaXterm.

## Objectives

* Launch an Ubuntu 24.04 EC2 instance on AWS.
* Establish an SSH connection using MobaXterm and the default `ubuntu` user.
* Set a password for the root account.
* Configure SSH settings to enable root login and password authentication.
* Validate the SSH configuration and restart the SSH service.
* Connect directly to the instance using the `root` username.

## Technologies Used

* **AWS EC2** – Virtual server hosting.
* **Ubuntu 24.04** – Operating system.
* **MobaXterm** – Remote SSH access.
* **OpenSSH** – Secure remote connection service.

## Configuration Summary

The SSH daemon configuration is modified to permit root login and password-based authentication. After validating and restarting the SSH service, a new MobaXterm session is configured to connect using the root account.

## Security Note

Direct root login and password-based SSH authentication increase security risks, particularly on internet-accessible servers. For production environments, it is recommended to use SSH key authentication, disable direct root login, and perform administrative tasks using `sudo`.

## Outcome

Successfully configuring direct root SSH access to an Ubuntu 24.04 EC2 instance using MobaXterm for learning and testing purposes.
