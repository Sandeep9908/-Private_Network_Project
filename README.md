# Private Network Project

This project demonstrates the setup of a private two-tier architecture using CentOS VMs in VirtualBox, including a web server and a database server connected over a host-only network.

### 1. Network Adapter Settings – Web Server  
Shows the web server's network interface configured with Host-Only Adapter.  
![Network Settings Screenshot](https://i.postimg.cc/HsVpy3gm/Screenshot-2025-07-28-130611.png)

### 2. VM Configuration Overview – General Settings  
Displays basic configuration settings of the virtual machine.  
![VM Setup Screenshot](https://i.postimg.cc/6pvms4dn/Screenshot-2025-07-28-124704.png)

### 3. Host-Only Adapter Connection Details  
Details of IP and adapter setup for internal communication.  
![Host-Only Adapter Details](https://i.postimg.cc/jSvLbcyJ/Screenshot-2025-07-28-132859.png)

### 4. Web Server – IP Address Check  
Output of `ip addr` showing assigned IP to web server VM.  
![Web Server IP Output](https://i.postimg.cc/WzR4nHcx/Screenshot-2025-07-28-133104.png)

### 5. Database Server – IP Address Check  
Displays internal IP for the database server on private network.  
![DB Server IP Output](https://i.postimg.cc/C1n1bVXj/Screenshot-2025-07-28-133239.png)

### 6. DB Service – Active Status  
Confirmation that MariaDB service is running successfully.  
![MariaDB Service Active](https://i.postimg.cc/ZKSRv2cd/Screenshot-2025-07-28-133831.png)

### 7. Apache Service – Active Status  
Apache HTTP server status check to confirm it's active.  
![Apache Active Screenshot](https://i.postimg.cc/QMyCBM48/Screenshot-2025-07-28-134100.png)

### 8. File Upload Web Page (User Form)  
Frontend form interface for user data and file upload.  
![User Form Interface](https://i.postimg.cc/cCQL5BsC/Screenshot-2025-07-28-134148.png)

### 9. File Upload Output – Confirmation Message  
Displays a successful file upload and user entry message.  
![Upload Confirmation Screenshot](https://i.postimg.cc/3rpNRYgh/Screenshot-2025-07-28-134159.png)

### 10. Data Saved in Database – phpMyAdmin View  
Shows uploaded data saved properly in the database table.  
![phpMyAdmin Screenshot](https://i.postimg.cc/15rzGBCY/Screenshot-2025-07-28-134237.png)


