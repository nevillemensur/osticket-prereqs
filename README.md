# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://youtu.be/8n1kV9wc6g8)

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

<h2>Installation Steps</h2>

<p>
Start by creating a resource group inside Microsoft Azure. This resource group is where will store our virtual machines.
</p>

<p>
<img src="https://i.imgur.com/TmqScaP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Name your resource group "RG-osticket" and select a region. I recommend using a region that is near you. Then click "Review+Create"
</p>

<p>
<img src="https://i.imgur.com/7BcAZb8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Create a virtual machine.
</p>

<p>
<img src="https://i.imgur.com/tuJOw9A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Create a virtual machine that runs on Windows and add it to the resource group labeled "RG-osticket"
</p>

<p>
<img src="https://i.imgur.com/q3SgSuI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Create a username and password. The username and password will be used to log into remote desktop.
</p>

<p>
<img src="https://i.imgur.com/QQFd529.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Copy the public IP address. The IP address will be used to connect to a PC in Microsoft remote desktop.
</p>

<p>
<img src="https://i.imgur.com/a16emO7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Paste the IP address from Microsoft Azure for the PC name.
</p>

<p>
<img src="https://i.imgur.com/qQgDCr1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Enter the username and password that was created in Azure.
</p>

<p>
<img src="https://i.imgur.com/Bl58TL8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<p>
Enable and install Information Internet Services (IIS)
  - Open run
  - Enter control panel
  - Click programs
  - Click "Turn window features on or off"
  - Click "Internet Information Services"
  - Click "World Wide Web Services"
  - Click "Application Development Features"
  -Select "CGI"
</p>

<p>
<img src="https://i.imgur.com/uZFyyR8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/T3jpiW4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
<img src="https://i.imgur.com/7mWt6ep.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
<img src="https://i.imgur.com/2oWq5Ec.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
<img src="https://i.imgur.com/mtDPKGK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
<img src="https://i.imgur.com/ZfR5hvJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/jBox0zh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
<img src="https://i.imgur.com/1VZzwj8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
Install PHP manager.
</p>

<p>
<img src="https://i.imgur.com/agalfVf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Install Rewrite module.
</p>

<p>
<img src="https://i.imgur.com/NVYBUEI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Create a directory in C:\\ drive -> create new folder -> name the folder PHP
</p>

<p>
<img src="https://i.imgur.com/al3ubNY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/iS8U6KY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/zExOycA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Install PHP 7.3.8 and unzip the contents in C:\PHP
</p>

<p>
<img src="https://i.imgur.com/DEiDZnx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/GIxzrR3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/dbEZYWP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Install C++
</p>

<p>
<img src="https://i.imgur.com/cNcGE6a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Install MySQL 5.5.62->
Typical Setup->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Password1

</p>

<p>
<img src="https://i.imgur.com/v9NCNCk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/IjTORha.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/ZSaurUe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/4SJu7Y7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/gKj7dWE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/eYOC620.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Open IIS as admin.
</p>

<p>
<img src="https://i.imgur.com/RSuRnuH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Register PHP from within IIS
</p>

<p>
<img src="https://i.imgur.com/lGEsyxq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/wBaUCXU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/vTS6nd9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/lX3T73O.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/RO2ESjt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Install osTicket v1.15.8
Download osTicket from the Installation Files Folder
Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

</p>

<p>
<img src="https://i.imgur.com/Tl55roA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/h66I96j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/YMWqJBe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/NP0X91J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/gGrPl9c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

</p>

<p>
<img src="https://i.imgur.com/UBcF7K6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/1XiJFwX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes
</p>

<p>
<img src="https://i.imgur.com/A3rp0SN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/Bnidzbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/ZVOWmQq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/HSebrEm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/b0VLVJr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/EwiUXbv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/RIMj6rG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
  
osTicket-> include -> ost-sampleconfig.php -> ost-config.php

</p>

<p>
<img src="https://i.imgur.com/LglHbRl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/Jf8qcEn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/zVVPjDA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/LDWFHQl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Assign Permissions: ost-config.php
Disable inheritance -> Remove All ->
New Permissions -> Everyone -> All

</p>

<p>
<img src="https://i.imgur.com/pnAXgPs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/zfxMeOP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
</p>
<br />

<p>
<img src="https://i.imgur.com/OY6j1Nk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/ysd3w7D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/72xpiNq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/ZDB6wwP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/KZE7d1o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/YbSYWW1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

</p>

<p>
<img src="https://i.imgur.com/j9Yu7W8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
From the Installation Files, download and install HeidiSQL.
  
Open Heidi SQL ->
Create a new session, root/Password1 ->
Connect to the session ->
Create a database called “osTicket”

</p>

<p>
<img src="https://i.imgur.com/7CIEQmH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/SzRFE6p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/fbPVBqE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/Ixl56a3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/IKBu3YU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Continue Setting up osticket in the browser
  
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!”

</p>

<p>
<img src="https://i.imgur.com/pKzFSIk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Congratulations, hopefully it is installed with no errors!
  
Browse to your help desk login page: http://localhost/osTicket/scp/login.php
  
Enter creditentals 

</p>

<p>
<img src="https://i.imgur.com/j8UisMg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/u7rhabP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
</p>
<br />

<p>
<img src="https://i.imgur.com/SM9UGqb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
Clean up
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>

<p>
<img src="https://i.imgur.com/w2wG0Jy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

</p>
<br />

<p>
<img src="https://i.imgur.com/abktXfv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/DDFR6iM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/O38Jue0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/FR3mqCh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/PG21JYv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
</p>
<br />

