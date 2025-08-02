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

- In Azure, locate and create a resouce group (using your free or paid subscription.
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

<h3> Step 2: Install a windows virtual machine</h3>

- In Azure, locate and create a virtual machine. (Windows 10 pro version 22H2).
- Name: osticket-vm.
- Reigon: East US 2.
- Size: 2vcpus, 8 GiB memory.

<h3> Set the username to "mr_admin" and password to "Password1"</h3>

- Check the box at the bottom of the page. 
- Review + Create.

<img src="https://i.imgur.com/97AR0Lv.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/S4IVNu7.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/i0EgI73.png" height="80%" width="80%"/>
<p> Great job! You've now created a resource group and a virtual machine within Microsoft Azure! </p>

<br> <br/> 

<h3> Step 3: Logging into our Virtual Machine (VM) through Remote Desktop and setting up osTicket </h3>

- In Azure, locate your osTicket-vm, and copy the public IP addresss.
- Paste it into your Remote Desktop 
- Sign in with "mr_admin" & "Passworrd1". 
- Hit yes and login. 
  
<img src="https://i.imgur.com/r0VgTNF.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/gzjTcAh.png" height="80%" width="80%"/>
<img src="https://i.imgur.com/uvuPkp8.png" height="80%" width="80%"/>

<br> <br/> 

<h3> Step 4:  </h3>

- 
- 
- 
- 

<img src=" " height="80%" width="80%"/>
<img src=" " height="80%" width="80%"/>
<img src=" " height="80%" width="80%"/>


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.







 
<br />
<p>
	<img src="https://i.imgur.com/8wvWH0H.jpg" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center"> Congrats, You've Finished Installing osTicket.</h3>
