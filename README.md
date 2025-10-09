# Deploying-osTicket-in-a-Windows-Server-Lab-Environment
📝 Project Summary

This project is a tutorial walkthrough demonstrating the full deployment and configuration of osTicket, an open-source support ticketing system, within a simulated IT infrastructure using virtual machines.

It replicates a small enterprise environment, showcasing key IT skills including domain controller setup, user/group management, LAMP stack deployment, and internal web access from client machines.

🔹 Languages Used:

PowerShell (for automation and user account creation)

Basic command line / Bash scripting (for Linux setup)

🔹 Environments Used:

Windows Server 2019 (Domain Controller, DNS)

Windows 10 (Client Machine)

Ubuntu 20.04 (Web Server)

Hyper-V (Virtualization)

🔹 Technologies / Applications / Services:

osTicket (Support Ticket System)

Apache, MySQL, PHP (LAMP stack)

Active Directory Domain Services

Remote Desktop Protocol (RDP)

Windows DNS Server

GitHub (Documentation repository)

📷 Media (Images & Video)
📸 Screenshots:

Hyper-V VM Setup


Active Directory Configuration


osTicket Installation Page


Ticket Creation from Client


Admin Panel Showing Submitted Ticket


 All images are located in the /media folder for clarity and organization.

🎥 Video Walkthrough :

📺 Watch Full Demo on YouTube

🧪 Demonstration

This section walks through each step of the project implementation in detail.

✅ Step 1: Set Up the Domain Controller (Windows Server 2019)

Configure a static IP

Rename the server and install Active Directory Domain Services

Promote to Domain Controller

Set up internal domain: corp.local

Create test user accounts in Active Directory

✅ Step 2: Set Up Ubuntu Web Server (Ubuntu 20.04)

Install Ubuntu on Hyper-V VM

Install Apache: sudo apt install apache2

Install MySQL: sudo apt install mysql-server

Install PHP and dependencies:
sudo apt install php libapache2-mod-php php-mysql php-imap php-intl php-gd php-curl php-mbstring php-xml php-cli unzip

Restart services and configure firewall:

sudo systemctl restart apache2
sudo ufw allow 80

✅ Step 3: Download and Install osTicket

Download osTicket from official site

Unzip and move to /var/www/html/

Create MySQL database and user

Run web-based setup at http://<ubuntu-ip>/upload

✅ Step 4: Connect Windows 10 Client to the Domain

Join the client to the domain corp.local

Log in with test AD account

Open browser and navigate to osTicket web server

Create a new support ticket

✅ Step 5: Ticket Handling

Admin logs into the osTicket dashboard

Views the ticket, assigns agent, replies

Demonstrates full ticket lifecycle

🏁 Conclusion

This project demonstrates the following core IT skills:

Server configuration and domain management

LAMP stack and application hosting

Cross-platform networking (Windows ↔ Linux)

User role simulation (End-user vs IT Support)

It also shows real-world implementation of a help desk system that employers often use, such as osTicket, ServiceNow, or Freshdesk.
