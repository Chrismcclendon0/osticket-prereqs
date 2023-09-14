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
Open IIS as an Admin. Register PHP from within IIS. Reload IIS (Open IIS, Stop and Start the server). Install osTicket v1.15.8 then download osTicket from the installation files folder. Extract and copy “upload” folder to c:\inetpub\wwwroot. Within c:\inetpub\wwwroot, rename “upload” to “osTicket”
</p>
<br />
