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
  <img width="776" height="476" src="https://github.com/user-attachments/assets/3ffa3332-99f5-4291-ad76-00455ceb5695" />
</p>

<p>
  I created a new Resource Group named <strong>osticket</strong> in Microsoft Azure. After that, I deployed a Virtual Machine using Windows 11 Pro as the operating system. During configuration, I selected a VM size that provides 2 vCPUs to ensure proper performance for the setup.
  Next, we will be connecting to the VM using Remote Desktop (RDP) using the public IP.
</p>

<br>

<h2>Connecting to the VM (RDP)</h2>

<p>
  <img width="478" height="284" src="https://github.com/user-attachments/assets/566f3d20-976a-4085-828a-0e2bd32abd26" />
</p>

<p>
  To connect to my VM, I used Remote Desktop Protocol (RDP). I grabbed the public IP address from the Azure VM overview page, opened the Remote Desktop app on my computer, typed in that IP, and connected to the VM. After that, we’ll cover settings that need to be enabled on the VM for osTicket and the files needed to install it.
</p>

<br>

<h2>Enabling IIS for CGI</h2>

<p>
  <img width="765" height="467" src="https://github.com/user-attachments/assets/adda132d-1f4f-4312-87ab-d0bf894ac799" />
</p>

<p>
  To run osTicket on Windows 11, we need to enable IIS and CGI/FastCGI so the system can act as a web server and run PHP files. You can turn these features on by going to <strong>Control Panel → Programs → Turn Windows features on or off</strong>, which prepares Windows to properly host and load osTicket. From here, we can move on to the files needed to run the program.
</p>

<br>

<h2>osTicket Installation Files</h2>

<p>
  <img src="https://github.com/user-attachments/assets/e8349ff5-36fe-4e04-9c49-459ab5f79c8c" height="250">
  <img src="https://github.com/user-attachments/assets/8e7d2416-4c08-42e2-976a-fe80ed32161a" height="250">
</p>

<p>
  Next, we’ll download the files needed to set up osTicket.  
  Download link:  
  https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0  
  Before installing anything else, we’ll start by installing PHP Manager for IIS, since osTicket relies on PHP to run its web pages.
</p>

<br>

<p>
  <img width="487" height="402" alt="image" src="https://github.com/user-attachments/assets/6b3b7811-5350-499d-b89b-a21d4039a311" />
  <img width="485" height="383" src="https://github.com/user-attachments/assets/cb00f76f-c517-43a4-b80d-561ab4b1b0be" />
</p>

<p>
  Once PHP Manager is done installing, we can proceed to downloading the Rewrite Module.
</p>

<br>

<p>
  <img width="735" height="468" src="https://github.com/user-attachments/assets/e2195eb0-2cfa-4918-8603-a429a4fb6ef2" />
</p>

<p>
  Before continuing, we need a place to extract the PHP files. Go to your <strong>C:\ drive</strong> and create a new folder named <strong>PHP</strong>. We’ll use this folder to unzip the PHP package from the installation files so it’s ready for IIS to use during the osTicket setup.
</p>

<br>

<p>
  <img width="471" height="291" src="https://github.com/user-attachments/assets/9bc65665-0d23-4a15-86a5-dd8cc89d5b74" />
</p>

<p>
  We’re almost done, so before the final step, we need to install <strong>VC_redist.x86</strong>, which adds the necessary Visual C++ components that PHP and osTicket rely on.
</p>

<br>

<p>
  <img width="485" height="380" src="https://github.com/user-attachments/assets/93a534e4-49ad-4f25-9f63-21243ed27d54" />
</p>

<p>
  The last step in the setup is installing <strong>MySQL</strong>, which will be used to store all of osTicket’s data, including tickets, users, and system settings. Once that is done we will launch the MySQL Wizzard and use the standard configuration.
</p>

<br>

<p>
  <img width="471" height="291" src="https://github.com/user-attachments/assets/9bc65665-0d23-4a15-86a5-dd8cc89d5b74" />
</p>

<p>
  We’re almost done, so before the final step, we need to install <strong>VC_redist.x86</strong>, which adds the necessary Visual C++ components that PHP and osTicket rely on.
</p>

<br>

<p>
  <img width="485" height="380" src="https://github.com/user-attachments/assets/93a534e4-49ad-4f25-9f63-21243ed27d54" />
</p>

<p>
  The last step in the setup is installing <strong>MySQL</strong>, which will be used to store all of osTicket’s data, including tickets, users, and system settings.
</p>

<br>
