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

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install IIS with CGI
- Intall PHP Manager for IIS
- Install Rewrite Module
- Install PHP 7.3.8
- Install VC Redist x86.exe.
- Install MySQL 5.5.62

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/chyaFyl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Verify that your server meets the minimum requirements for osTicket, such as PHP version, database support, and web server compatibility.
</p>
<br />

<p>
<img src="https://i.imgur.com/chyaFyl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Visit the official osTicket website or GitHub repository.
Download the latest stable version of osTicket in ZIP format.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Unzip the downloaded file to a directory on your server.
Make sure the web server has read and write permissions to this directory.
</p>

<p>
<img src="https://i.imgur.com/chyaFyl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a new MySQL or MariaDB database for osTicket.
Note down the database name, username, and password for later use.
</p>
<br />

<p>
<img src="https://i.imgur.com/chyaFyl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure your web server (e.g., Apache, Nginx) to serve the osTicket files.
Set up a virtual host or configure the root directory of your web server to point to the osTicket installation directory.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open a web browser and navigate to the URL where you installed osTicket.
Follow the installation wizard instructions.
Provide the database details (name, username, password) when prompted.
Create an administrator account with a username and password.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After successful installation, remove the setup directory from the osTicket installation folder for security purposes.
Log in to the osTicket admin panel using the administrator account credentials.
</p>
<br />
