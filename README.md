<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11 (25H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machines
- osTicket installation files
- Hidi SQL

<h2>Virtual Machine Setup</h2>


<p>
<img width="776" height="476" alt="Screenshot 2025-11-30 181319" src="https://github.com/user-attachments/assets/3ffa3332-99f5-4291-ad76-00455ceb5695" />
</p>
<p>
I created a new Resource Group named osticket in Microsoft Azure. After that, I deployed a Virtual Machine using Windows 11 pro as the operating system. During configuration, I selected a VM size that provides 2 vCPUs to ensure proper performance for the setup. Next we will be connecting to the VM using Remote Desktop (RDP) using the public IP.
</p>
<br />
<h2>Connecting to the VM (RDP)</h2>
<p>
<img width="478" height="284" alt="Screenshot 2025-11-30 181645" src="https://github.com/user-attachments/assets/566f3d20-976a-4085-828a-0e2bd32abd26" />
</p>
<p>
To connect to my VM, I used Remote Desktop Protocol (RDP). I grabbed the public IP address from the Azure VM overview page, opened the Remote Desktop app on my computer, typed in that IP, and connected to the VM. After that, we’ll cover settings that need to be enbaled on the VM for osTicket and the files needed to install it.
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To run osTicket on Windows 11, we need to enable IIS and CGI/FastCGI so the system can act as a web server and run PHP files. You can turn these features on by going to Control Panel → Programs → Turn Windows features on or off, which prepares Windows to properly host and load osTicket.
</p>
<br />
