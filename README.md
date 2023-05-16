<p align="center">
<img src="" alt="osTicket logo"/>
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
<img src= "https://i.imgur.com/5LT9dmY.png" height="80%" width="80%" alt="ISS Steps"/>
</p>
<p>
Install / Enable IIS in Windows WITH CGI
</p>
<br />

<p>
<img src="https://i.imgur.com/UmF4Tav.png" height="80%" width="80%" alt="PHP Manager"/>
</p>
<p>
Download and install PHP Manager for IIS:

Visit the official Microsoft website for PHP Manager for IIS.
Download the "PHPManagerForIIS_V1.5.0.msi" file.
Run the downloaded file and follow the on-screen instructions to install PHP Manager for IIS.

</p>
<br />

<p>
<img src="https://i.imgur.com/N50YjL3.png" height="80%" width="80%" alt="Rewrite Module"/>
</p>
<p>
Download and install the Rewrite Module:

Download the "rewrite_amd64_en-US.msi" file for the Rewrite Module.
Run the downloaded file and follow the installation instructions to install the Rewrite Module.
</p>

<p>
<img src="https://i.imgur.com/hsTOjTr.png" height="80%" width="80%" alt="PHP 7.3.8"/>
</p>
<p>
Download and unzip PHP 7.3.8:

Download the "php-7.3.8-nts-Win32-VC15-x86.zip" file for PHP 7.3.8.
Extract the contents of the ZIP file.
Create a directory named "C:\PHP".
Copy the extracted files from the PHP folder to the "C:\PHP" directory.
</p>
<br />

<p>
<img src="https://i.imgur.com/BwqTLWl.png" height="80%" width="80%" alt="VC redist"/>
</p>
<p>
Download and install VC_redist.x86.exe:

Download the "VC_redist.x86.exe" file.
Run the downloaded file and follow the installation instructions to install the Visual C++ Redistributable for Visual Studio.
</p>
<br />

<p>
<img src="https://i.imgur.com/NKQS2pO.png" height="80%" width="80%" alt="MySQL"/>
</p>
<p>
Download and install MySQL 5.5.62:

Download the "mysql-5.5.62-win32.msi" file for MySQL 5.5.62.
Run the downloaded file and follow the installation instructions to install MySQL.
</p>
<p>
Launch Configuration Wizard for MySQL:

Launch the MySQL Configuration Wizard after the installation.
  Typical Setup ->
  Launch Configuration Wizard (after install) ->
  Standard Configuration ->
  Password1
</p>
<br />

<p>
<img src="https://i.imgur.com/ZdBGhSH.png" height="80%" width="80%" alt="IIS Administration"/>
</p>
<p>
Open IIS as an Admin:

Open Internet Information Services (IIS) Manager.
Run it as an administrator to have the necessary permissions.
</p>
<br />

<p>
<img src="https://i.imgur.com/hsTOjTr.png" height="80%" width="80%" alt="Register PHP
</p>
<p>
Register PHP from within IIS:

In IIS Manager, select the server node.
Double-click on "PHP Manager" to open it.
Click on "Register new PHP version" and browse to the "php-cgi.exe" file in the "C:\PHP" directory.
Select the newly registered PHP version.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZrcmRqr.png" height="80%" width="80%" alt="Reload IIS"/>
</p>
<p>
Reload IIS:

In IIS Manager, click on the server node.
Click on "Restart" in the right-hand panel to reload IIS.
</p>

<p>
<img src="https://i.imgur.com/wdoLyp1.png" height="80%" width="80%" alt="Install osTicket"/>
</p>
<p>
Install osTicket v1.15.8:

Download osTicket from the installation files folder.
Extract the contents of the ZIP file.
Rename the extracted "upload" folder to "osTicket".
Copy the "osTicket" folder to "C:\inetpub\wwwroot".
 Reload IIS
</p>
<br />

<p>
<img src="https://i.imgur.com/Zu9OHRp.png" height="80%" width="80%" alt="Browse *:80 "/>
</p>
<p>
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
</p>

<p>
<img src="https://i.imgur.com/P3nDeMc.png" height="80%" width="80%" alt="Extensions not enabled"/>
  
<img src="https://i.imgur.com/akWGsZW.png" height="80%" width="80%" alt="Enable Extensions"/>
</p>
<p>

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes

</p>
<br />

<p>
<img src="https://i.imgur.com/vMjkA1l.png" height="80%" width="80%" alt="Set Permissions"/>
</p>
<p>
Set Permissions for ost-config.php:

Go to "C:\inetpub\wwwroot\osTicket\include".
Rename "ost-sampleconfig.php" to "ost-config.php".
Right-click on "ost-config.php" and select "Properties".
</p>
<br /><p>
<img src="https://i.imgur.com/XhT3A7C.png" height="80%" width="80%" alt="Disable inheritance"/>
  <img src="https://i.imgur.com/glBR3Ey.png" height="80%" width="80%" alt="New Permissions"/>
</p>

<p>
Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All


</p>

<p>
<img src="https://i.imgur.com/9B1RyxH.png" height="80%" width="80%" alt="Download and install HeidiSQL"/>
 
  <img src="https://i.imgur.com/cq00b9h.png" height="80%" width="80%" alt="Create database"/>
</p>
<p>
Download and install HeidiSQL.
Open Heidi SQL
Create a new session, root/Password1
Connect to the session
Create a database called “osTicket”

</p>

<p>
<img src="https://i.imgur.com/XFsTzdY.png" height="80%" width="80%" alt="Configure osTicket"/>
</p>
<p>
Configure osTicket:

Follow the on-screen instructions to continue setting up osTicket.
Provide the requested information, such as the Helpdesk name and default email.
When prompted for the database, use the following details:
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click on "Install Now!" to complete the installation.

</p>
<p>
Clean up
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

