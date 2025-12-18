<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" width="220"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
<p>This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.</p>

<br>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<br>

<h2>Operating Systems Used</h2>

- Windows 11 (25H2)

<br>

<h2>List of Prerequisites</h2>

- Azure Virtual Machines
- osTicket installation files
- HeidiSQL

<br>

<h2>Virtual Machine Setup</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/3ffa3332-99f5-4291-ad76-00455ceb5695" width="800" alt="Azure VM setup" />
</p>

<p>
  I created a new Resource Group named <strong>osticket</strong> in Microsoft Azure. After that, I deployed a Virtual Machine using Windows 11 Pro as the operating system. During configuration, I selected a VM size that provides 2 vCPUs to ensure proper performance for the setup. Next, we will be connecting to the VM using Remote Desktop (RDP) using the public IP.
</p>

<br>

<h2>Connecting to the VM (RDP)</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/566f3d20-976a-4085-828a-0e2bd32abd26" width="800" alt="RDP connection" />
</p>

<p>
  To connect to my VM, I used Remote Desktop Protocol (RDP). I grabbed the public IP address from the Azure VM overview page, opened the Remote Desktop app on my computer, typed in that IP, and connected to the VM. After that, we’ll cover settings that need to be enabled on the VM for osTicket and the files needed to install it.
</p>

<br>

<h2>Enabling IIS for CGI</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/adda132d-1f4f-4312-87ab-d0bf894ac799" width="800" alt="Enable IIS and CGI" />
</p>

<p>
  To run osTicket on Windows 11, we need to enable IIS and CGI/FastCGI so the system can act as a web server and run PHP files. You can turn these features on by going to <strong>Control Panel → Programs → Turn Windows features on or off</strong>, which prepares Windows to properly host and load osTicket. From here, we can move on to the files needed to run the program.
</p>

<br>

<h2>osTicket Installation Files</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/e8349ff5-36fe-4e04-9c49-459ab5f79c8c" width="390" alt="Download files 1">
  <img src="https://github.com/user-attachments/assets/8e7d2416-4c08-42e2-976a-fe80ed32161a" width="390" alt="Download files 2">
</p>

<p>
  Next, we’ll download the files needed to set up osTicket.<br>
  Download link:<br>
  https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&au
