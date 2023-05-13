# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a resource group in Azure
- Create an Azure virtual machine windows 10, 4 vCPUs
- Add your PC connection in Microsoft Remote Desktop
- Enable Internet Information Services (IIS) WITH CGI
- Download and install PHP manager
- Download and install Rewrite module
- Create a directory folder in Windows C drive and label the folder PHP
- Download and install PHP 7.3.8
- Download and install C++
- Download and install My SQL server
- Open (IIS) as an Admin
- Register PHP from within IIS
- Reload IIS (Open, stop, start server)
- Install os ticket 
- Extract and copy "upload" folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot rename "upload" to "osticket"
- Reload IIS (Open, stop, start server)
- Go to sites -> default -> os ticket-> click *browse 80
- Go back to IIS, sites-> default-> osticket
- Double click PHP manager
- Click "enable or disable and extension"
- Enable php_impap.dll , php_intl.dll , php_opache.dll
- Refresh the osTicket site in your browse, observe the changes
- Rename ost-config.php 
- From C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php
- Assign permissions: ost-config.php
- Disable inheritance-> Remove All
- New Permissions-> Everyone-> All
- Continue Setting up osTicket -> create helpdesk name -> create default email
- Download and install HeidiSQL
- Open Heidi SQl -> create a new session, root/Password1 -> connect to the session -> create a database called "osTicket"
- Continue setting up osticet in the browser
- MySQL Database
- MySQL Username
- MySQL Password
- Install Now
- Browse to your help desk login page
- Clean Up
- Delete C:\inetpub\wwwroot\osTicket\setup
- Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
- Item 5
- Item 5

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
