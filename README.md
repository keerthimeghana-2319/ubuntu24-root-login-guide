# AWS EC2 Ubuntu 24: Direct Root SSH Configuration Guide

A step-by-step documentation on setting up an Ubuntu EC2 instance on AWS and enabling direct SSH login for the `root` user with password authentication.

---

## 1. Launch & Identify Instance
* Launch an Ubuntu 24.04 instance on AWS EC2.
* Note down the instance's **Public IPv4 address** and ensure SSH (Port 22) is open in the attached Security Group.

![EC2 Instance](images/01-ec2-instance.png)

---

## 2. Initial SSH Connection via MobaXterm
* Open MobaXterm and create a new SSH session.
* Use default username `ubuntu` and attach your downloaded `.pem` key under **Advanced SSH settings**.
* Successfully access the terminal.

![MobaXterm Initial SSH](images/02-initial-ssh.png)

---

## 3. Set Root Password
Switch to root and set a strong password:
bash
sudo su
passwd root
![Set Root Password](images/03-root-password.png)

---

## 4. Modify SSH Daemon Configuration
Edit the SSH server configuration file:
Update or add the following directives:
[200~text
PermitRootLogin yes
PubkeyAuthentication no
PasswordAuthentication yes
KbdInteractiveAuthentication yes~
![SSHD Configuration 1](images/04-sshd-config-1.png)
![SSHD Configuration 2](images/05-sshd-config-2.png)

---

## 5. Validate & Restart SSH Service
Check the syntax and reload the SSH daemon:
[200~
bash
sshd -t
systemctl restart ssh
![Restart SSH](images/06-restart-ssh.png)

---

## 6. Connect Directly as Root
* Create a new session in MobaXterm with Remote Host set to your Public IP and username set to `root`.
* Authenticate using the password configured in Step 3.

![Connect Root](images/07-connect-root.png)
![Root Password Prompt](images/08-root-prompt.png)
