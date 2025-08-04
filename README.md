<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>File needed for osTicket (download it anyway, it's safe I promise)</h2>

- ### [osTicket downloadedable installation file](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>What's needed for the installation?</h2>

- Microsoft Azure account with an active subscription (free or paid) 
- An active resource group.
- An active virtual network and subnet.
- An actince VM (virtual machine).
- An active RDP (remote desktop protocol).

<h2>Installation Steps</h2>
<br/> 
<h3> Step 1: Creating the resource group </h3>

- In Azure, locate and create a resource group (using your free or paid subscription.
- Name: osticket

<p>
<img src="https://i.imgur.com/9HJuej8.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/B2IkeSq.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/4PpCaLo.png" height="80%" width="80%"/>
	
</p>
<p>
You should have something similar to this.
</p>
<br />

<h3> Step 2: Install a Windows virtual machine</h3>

- In Azure, locate and create a virtual machine. (Windows 10 Pro version 22H2).
- Name: osticket-vm.
- Region: East US 2.
- Size: 2vcpus, 8 GiB memory.

<h3> Set the username to "mr_admin" and password to "Password1"</h3>

- Check the box at the bottom of the page. 
- Review + Create.

<img src="https://i.imgur.com/97AR0Lv.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/S4IVNu7.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/i0EgI73.png" height="80%" width="80%"/>
<p> Great job! You've now created a resource group and a virtual machine within Microsoft Azure! </p>

<br> <br/> 

<h3> Step 3: Logging into our Virtual Machine (VM) through Remote Desktop </h3>

- In Azure, locate your osTicket-vm, and copy the public IP address.
- Paste it into your Remote Desktop 
- Sign in with "mr_admin" & "Passworrd1". 
- Hit yes and login. 
  
<img src="https://i.imgur.com/r0VgTNF.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/gzjTcAh.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/uvuPkp8.png" height="80%" width="80%"/>
<p> bada boom, bada bing.<p/>  

<br> <br/> 

<h3> Step 4: Download the osTicket installation files on the remote desktop and follow through.</h3>

- ### [osTicket downloadedable installation file](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)
  
<img src="https://i.imgur.com/qyqBJss.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/C4Ec9qO.png" height="80%" width="80%"/> 

- Install / Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CGI
<img src= "https://i.imgur.com/AWpVfRu.png" height="80%" width="80%"/> 
<img src="https://i.imgur.com/iwmN7om.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/iWprBY8.png" height="80%" width="80%"/>

<p> From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)<p/> 
<img src="https://i.imgur.com/kGtsmNZ.png" height="80%" width="80%"/>

- Create the directory C:\PHP
- From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
<img src="https://i.imgur.com/TenSH4E.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/cIIaab3.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/dME0xKc.png" height="80%" width="80%"/>

- From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.

<img src="https://i.imgur.com/mVHMpPI.png" height="80%" width="80%"/>

- From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)

- Typical Setup 
- Launch Configuration Wizard (after install) 
- Standard Configuration 
- Username: root
- Password: root
<img src="https://i.imgur.com/hXgqM8g.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/f2EwndP.png" height="80%" width="80%"/> 
<img src="https://i.imgur.com/QUmAFjm.png" height="80%" width="80%"/>
  Nice!
  <br> <br/>
  
  <h3> Step 5: IIS and more, we're almost finished!</h3>

- Open IIS as an Admin
- Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
- Reload IIS (Open IIS, Stop, and Start the server)
<img src="https://i.imgur.com/SoJmCJL.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/Edsom8D.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/LflMXkC.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/J263p4P.png" height="80%" width="80%"/>
Like so.
<br><br/> 
- Install osTicket v1.15.8
- From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”

- Within “c:\inetpub\wwwroot”, rename “upload” to “osTicket”

- Reload IIS (Open IIS, Stop and Start the server)
<img src="https://i.imgur.com/Bsswuei.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/8MMCQeo.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/9sPTocU.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/vXdcQht.png" height="80%" width="80%"/>

Now you're getting the hang of this! 
<br><br/> 
<h3> Step 5: Loading osTicket site & enabling php configurations</h3> 
- Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
<img src="https://i.imgur.com/tN2ArMw.png" height="80%" width="80%"/> 
<img src="https://i.imgur.com/LN2ttFC.png" height="80%" width="80%"/> 
 Note that some extensions are not enabled, let's fix this. 
- Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
<img src="https://i.imgur.com/Ow54wQc.png" height="80%" width="80%"/> 
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
<img src="https://i.imgur.com/cwvoePB.png" height="80%" width="80%"/> 
- Refresh the osTicket site in your browser, and observe the changes 

<br><br/> 
<h3> Step 6: ost-config.php and setting up osTicket in browser</h3> 
- Rename: ost-config.php

- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
  
<img src="https://i.imgur.com/XsLw366.png" height="80%" width="80%"/> 
<img src="https://i.imgur.com/NZwlZ3r.png" height="80%" width="80%"/> 
<img src="https://i.imgur.com/BoN8UST.png" height="80%" width="80%"/> 


- Assign Permissions: ost-config.php
  
- Disable inheritance -> Remove All
  
- New Permissions -> Everyone -> All

<img src="https://i.imgur.com/zLpUQSN.png" height="80%" width="80%"/> 
<img src="https://i.imgur.com/DuarEqo.png" height="80%" width="80%"/> 
<img src="https://i.imgur.com/3EodYUM.png" height="80%" width="80%"/> 
Perfecto. 
<br><br/> 
<h3> Step 7: Continue Setting up osTicket in the browser and database in HeidiSQL </h3> 

- Name Helpdesk
  
- Default email (receives email from customers)
<img src="https://i.imgur.com/wgaBoNd.png" height="80%" width="80%"/>

- From the “osTicket-Installation-Files” folder, install HeidiSQL.
- Open Heidi SQL
  
- Create a new session, root/root
<img src="https://i.imgur.com/jgvyprk.png" height="80%" width="80%"/> 

- Connect to the session
  
- Create a database called “osTicket”
<img src="https://i.imgur.com/uf6bg0W.png" height="80%" width="80%"/> 
<img src="https://i.imgur.com/OQC2Y9L.png" height="80%" width="80%"/> 

- Continue setting up osTicket in the browser
- MySQL Database: osTicket
  
- MySQL Username: root
  
- MySQL Password: root
  
- Click “Install Now!”

<img src="https://i.imgur.com/8GJrHR3.png" height="80%" width="80%"/> 
<img src="https://i.imgur.com/ktjWkz7.png" height="80%" width="80%"/> 
Congrats! 
<br><br/> 
<h3> Step 8: Sign in as adminuser to verify that everything is working correctly. </h3>
<img src="https://i.imgur.com/WhLoX12.png" height="80%" width="80%"/> 
<img src="https://i.imgur.com/Zl06v5z.png" height="80%" width="80%"/>
Looks like it checks out! 

<p>
</p>
<p>

</p>
<br />
<br />
<h3 align="center"> Congrats, You've Finished Installing osTicket.</h3>
