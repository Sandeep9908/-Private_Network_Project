# Private Network Project

This project demonstrates the setup of a private two-tier architecture using CentOS VMs in VirtualBox. It includes a web server and a database server connected over a host-only network, simulating real-world application deployment with internal communication.

---

# 🖥️ Private Network Project

> A two-tier architecture using **VirtualBox** with **CentOS** VMs: one as a **Web Server** and the other as a **Database Server**, connected via a private/internal network. The web server hosts a PHP application that connects to a MySQL/MariaDB database running on the second VM.

---

## 🔧 Project Setup Steps

### 1. Download and Install VirtualBox
- Get the latest version from: [https://www.virtualbox.org](https://www.virtualbox.org)
- Install it on your system.

### 2. Download CentOS ISO
- Visit: [https://www.centos.org](https://www.centos.org)
- Prefer **CentOS 7 Minimal ISO** for performance and simplicity.

---

## 💡 Create Virtual Machines

### 3. Create VM 1: Web Server
- Name: `WebServer`
- Type: Linux → Red Hat (64-bit)
- RAM: 2GB  
- HDD: 20GB (dynamically allocated)

### 4. Create VM 2: Database Server
- Name: `DBServer`
- Type: Linux → Red Hat (64-bit)
- RAM: 2GB  
- HDD: 20GB

---

## 📀 Install CentOS on Both VMs

### 5. Attach CentOS ISO
- Go to **Settings > Storage** on both VMs
- Attach the CentOS ISO as boot disk

### 6. Install CentOS
- Boot into ISO and install CentOS on both machines
- Set hostname:
  - WebServer → `webserver.local`
  - DBServer → `dbserver.local`

---

## 🌐 Configure Network

### 7. Set Network Type (Internal or Host-Only)
- In VirtualBox → Settings → Network for both VMs:
  - **Adapter 1**: Enable → Attached to: **Internal Network**
  - Name: `intnet` (same for both)

### Install Apache (Both VMs)
- sudo yum install httpd -y
- sudo systemctl enable httpd
- sudo systemctl start httpd
### Install PHP (Only on WebServer)
- sudo yum install php php-mysql -y

### Install sql (Only on DBServer)
  - Install MySQL Server in DB Server
  - Command : dnf -y install mysql-server 

### Database Setup
- mysql -u root -p
- CREATE DATABASE webapp;
- CREATE USER 'udc123'@'%' IDENTIFIED BY 'root@123';
- GRANT ALL PRIVILEGES ON udc.* TO 'udc123'@'%';

  



## 📸 Screenshots

### 1. Network Adapter Settings – Web Server  
Shows the web server's network interface configured with Host-Only Adapter.  
![Network Settings Screenshot](https://i.postimg.cc/HsVpy3gm/Screenshot-2025-07-28-130611.png)

### 2. Database Server – Network IP Address in Configuration  
Displays the internal private IP of the database server used in PHP connection settings.  
![Database Server IP in Config]

### 3. Host-Only Network Configuration – VirtualBox Global Settings  
Displays host-only network details from VirtualBox global settings.  
![Host-Only Network Global Config](https://i.postimg.cc/632kQbZb/Screenshot-2025-07-28-131548.png)

### 4. VM Configuration Overview – General Settings  
Displays basic configuration settings of the virtual machine.  
![VM Setup Screenshot](https://i.postimg.cc/6pvms4dn/Screenshot-2025-07-28-124704.png)

### 5. Host-Only Adapter Connection Details  
Details of IP and adapter setup for internal communication.  
![Host-Only Adapter Details](https://i.postimg.cc/jSvLbcyJ/Screenshot-2025-07-28-132859.png)

### 6. Web Server – IP Address Check  
Output of `ip addr` showing assigned IP to web server VM.  
![Web Server IP Output](https://i.postimg.cc/WzR4nHcx/Screenshot-2025-07-28-133104.png)

### 7. Database Server – IP Address Check  
Displays internal IP for the database server on private network.  
![DB Server IP Output](https://i.postimg.cc/C1n1bVXj/Screenshot-2025-07-28-133239.png)

### 8. DB Service – Active Status  
Confirmation that MariaDB (MySQL) service is running successfully.  
![MariaDB Service Active](https://i.postimg.cc/ZKSRv2cd/Screenshot-2025-07-28-133831.png)

### 9. Apache Service – Active Status  
Apache HTTP server status check to confirm it's active.  
![Apache Active Screenshot](https://i.postimg.cc/QMyCBM48/Screenshot-2025-07-28-134100.png)

### 10. File Upload Web Page (User Form)  
Frontend form interface for user data entry and file upload.  
![User Form Interface](https://i.postimg.cc/cCQL5BsC/Screenshot-2025-07-28-134148.png)

### 11. File Upload Output – Confirmation Message  
Displays a successful file upload and user confirmation message.  
![Upload Confirmation Screenshot](https://i.postimg.cc/3rpNRYgh/Screenshot-2025-07-28-134159.png)


