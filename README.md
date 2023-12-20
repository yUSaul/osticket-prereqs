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
- Download and install HeidiSQL
  
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
Use the executables to Install PHP manager, AMD Rewrite module, and VC_redist.  Install MySQL.  Typical Setup.  Launch the Instance Configuration Wizard.  Standard Configuration.  Password1 for root password.  OSTicket will use the MySQL database to store ticket data. 
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
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/e7f8fb3d-548f-4bdd-8061-4090477a188a"/>
</p>
<p>
Open IIS and register PHP.  Reload IIS after registering.
</p>
<br />

<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/9f580563-b1bb-421e-8b39-41646b8a6cde"/>
</p>
<p>
Download osTicket.  Extract and copy “upload” folder to c:\inetpub\wwwroot.  This is our IIS server folder.  Within c:\inetpub\wwwroot, rename “upload” to “osTicket”.
<br />

<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/36282fda-5b4a-415e-a23b-23e425401c93"/>
</p>
<p>
Go back to IIS, and restart the server.  Then go to Sites -> Default Web Site -> osTicket.  Click browse *.80 on the right.
</p>
<br />


<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/fb1f711b-faa6-4bb8-ac30-05c41efc926f"/>
</p>
<p>
Note that some of the extensions are disabled.  Go back to IIS, Sites -> Default Web Site -> osTicket.  Double-click PHP Manager.  Click “Enable or disable an extension”.  Enable: php_imap.dll.  Enable: php_intl.dll.  Enable: php_opcache.dll.  Refresh the osTicket site in your browser, and observe the changes.
</p>
<br />


<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/12faf829-94f9-4e41-98e3-0361c7ddf768"/>
</p>
<p>
Go to C:\inetpub\wwwroot\osTicket\include and look for ost-sampleconfig.php.  Rename this to ost-config.php.  Right click the file and then go to properties -> security -> advanced and disable inheritance.  Add a permission entry with Everyone as principal, giving Full control.
</p>
<br />


<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/e0f6f7e7-61af-424a-a97d-ea6a9642475e"/>
</p>
<p>
Continue in the browser by configuring osTicket.  Install HeidiSQL prior to clicking Install Now on the browser.
</p>
<br />


<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/0aaba12a-6dc5-4a3b-bebc-c64fb63ca3e3"/>
</p>
<p>
In HeidiSQL create a new connection with name root and the previously created SQL password.  Right click on Unnamed, go to Create New -> Database.  Name it osTicket. 
</p>
<br />

<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/6df4b909-e14e-4cc6-962f-d5d353643306"/>
</p>
<p>
Finish filling out the rest of the osTicket page on your browser with the SQL server info, then click Install Now.
</p>
<br />

<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/0aaba12a-6dc5-4a3b-bebc-c64fb63ca3e3"/>
</p>
<p>
osTicket is now succesfully installed.  To browse to your help desk login page: http://localhost/osTicket/scp/login.php.  End Users osTicket URL: http://localhost/osTicket.  Now set Permissions to Read and Read & Execute only in: C:\inetpub\wwwroot\osTicket\include\ost-config.php -> properties -> security -> advanced.
</p>
<br />

<p>
<img src="https://github.com/yUSaul/osticket-prereqs/assets/140694677/0aaba12a-6dc5-4a3b-bebc-c64fb63ca3e3"/>
</p>
<p>
In HeidiSQL create a new connection with name root and the previously created SQL password.
</p>
<br />
