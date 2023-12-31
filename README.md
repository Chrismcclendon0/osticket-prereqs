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

- Windows 10+
- Microsoft Azure Tenant 
- Microsoft Azure subscription
- (Installation Files) https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/f8d2ca82-0297-4bfb-883a-e33322df86e3)

</p>
<p>
First enter the official Microsoft Azure website and create your subscrption and tenant. Using the search bar, type and select "virtual machines", and click create. </p>
<br />

![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/ae086b52-5eba-4c8c-a8c3-650289d97519)


</p>
<p>
Allow Azure to auto create a resource group. Name your virtual machine, select desired region, and change "Image" to "Windows 10". Once completed create your username and passsword followed by confirming your "Licensing" by checking the respective box. 

</p>
<br />


![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/f09c04be-5c99-41b5-870d-41677ffa73a6)

</p>
<p>
Next select the "Networking" tab and confirm that the "Virtual network, subnet, and Public IP" will all be created by default. Once completed select "Review and create" to create your virtual machine.

  ![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/1383c720-5029-45f8-8431-528cbb3f3719)

Select your newly made virtual machine, copy the public IP address and enter it into remote desktop as a new user. Enter the username and password then connect.

![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/b655a02c-21a9-4297-9811-9897099a86a4)

Open the installation files included in the "Prerequsites" section and install Internet information Services (IIS). Enable IIS in windows with CGI and Common HTTP features, and IIS Management Console. From the installation files download and install "PHP Manager for IIS", "Rewrite Module". Create the directory "C:\PHP" then download "PHP 7.3.8" from the installation files and unzip the contents into C:\PHP.

![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/86f49cb9-b331-4346-b1b6-1880453c3a82)

![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/8e91973c-9705-4678-ab75-f2c79a0791f0)

Open IIS as an Admin. Register PHP from within IIS. Reload IIS (Open IIS, Stop and Start the server). Install osTicket v1.15.8 then download osTicket from the installation files folder. Extract and copy “upload” folder to c:\inetpub\wwwroot. Within c:\inetpub\wwwroot, rename “upload” to “osTicket”

![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/e6489fdc-424a-499d-a507-7ed0118ededa)
![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/c6791003-9f03-4f99-9ce3-09ef914b60c3)

Note that some extensions are not enabled. Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager. Click “Enable or disable an extension”
Enable: php_imap.dll,
Enable: php_intl.dll,
Enable: php_opcache.dll.
Refresh the osTicket site in your browse, observe the changes

![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/b014ae16-bd90-46da-8cb2-5d893391d6dd)
![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/ad10d355-a7a7-4adb-9df4-7f2891a8ed98)
Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php. Assign Permissions: ost-config.php. Disable inheritance -> Remove All, New Permissions -> Everyone -> All.
Continue Setting up osTicket in the browser (click Continue). Name Helpdesk. Default email (receives email from customers).



![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/0710eb8c-2644-4915-b343-5dbeb30eaf17)
![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/849f9155-dc64-4fbd-97d1-e61846d3e9af)

![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/9b91395d-d570-483e-b32f-2a4cecb69010)


From the Installation Files, download and install HeidiSQL. Open Heidi SQL Create a new session, root/Password. Connect to the session. Create a database called “osTicket”.
Continue Setting up osticket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!”

![image](https://github.com/Chrismcclendon0/osticket-prereqs/assets/144953146/fc76f679-2fd7-4ff3-bc43-306169612bdf)

Congratulations, hopefully it is installed with no errors!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php
</p>
<br />
