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

- Install / Enable IIS in Windows WITH CGI and Common HTTP Features AND IIS Management Console
- Download and install PHP Manager for IIS 
- Download and install the Rewrite Module 
- Create the directory C:\PHP, then download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
- Download and install VC_redist.x86.exe
- Download and install MySQL 5.5.62
  
<h2>Installation Steps</h2>

<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/a49b47b4-fea7-4bbd-b043-17f56489b691"/>
</p>
<p>
Start off by creating a Virtual Machine in Azure.  Create a Resource Group.  Create a Windows 10 Virtual Machine (VM) with 4 Virtual CPUs.  When creating the VM, allow it to create a new Virtual Network (Vnet).
</p>
<br />

<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/01b1db31-eed9-4465-a932-42a2b13f619d"/>
</p>
<p>
Install / Enable IIS in Windows WITH CGI and Common HTTP Features AND IIS Management Console
World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
Internet Information Services -> Web Management Tools -> IIS Management Console
[X] IIS Management Console
Using localhost 127.0.0.1 and getting an IIS webpage means that IIS has been succesfully installed.
</p>
<br />

<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/05876f79-6f0b-4665-9a66-c0aeab534af4"/>
</p>
<p>
Use the executables to Install PHP manager, AMD Rewrite module, and VC_redist. 
</p>
<br />

<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/6c6780af-5e9a-4f42-9f01-ca63371523c2"/>
</p>
<p>
Create the directory C:\PHP.  Download the PHP zip file and extract the contents into C:\PHP.
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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
