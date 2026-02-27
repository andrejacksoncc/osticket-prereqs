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

- PHP: A server-side scripting language needed for osTicket’s backend logic.
- PHP Manager for IIS: Helps configure and manage PHP with IIS.
- Rewrite Module: An IIS extension used for URL rewriting, required by osTicket.
- Microsoft Visual C++ Redistributable: Supports running certain PHP components.
- MySQL: The database server that stores all osTicket data (like tickets, users, etc.).

<h2>Installation Steps</h2>

<img width="80%" height="80%" alt="1" src="https://github.com/user-attachments/assets/bef7b6aa-e151-4906-a6a6-32db0272c344" />

- First create a new virtual machine in Azure with these specifications.
- Create a new resource group titled "osTicket".
- Select "(US) East US 2" as the region.
- Choose "Windows 10 Enterprise LTSC 2021 - x64 Gen2" for the image.
</p>
<br />

<img width="80%" height="80%" alt="2" src="https://github.com/user-attachments/assets/5ff9ca15-350c-4359-9be7-b23e8dbd3c20" />

- For the size choose any option that has "2 vcpus".
- Create a username and password for the virtual machine.
- Make sure to check the box at the bottom left that confirms you have eligible hosting rights.
- Click "Review + create" at the bottom and let azure create the virtual machine.
</p>
<br />

<img width="80%" height="80%" alt="3" src="https://github.com/user-attachments/assets/6ab005c9-af2b-45f7-8301-f34fec1827ca" />

- Once the virtual machine is done being created you can click on the newly created vm to get to this screen and obtain the public IP address.
</p>
<br />

<img width="80%" height="80%" alt="4" src="https://github.com/user-attachments/assets/d032bd28-0f3d-46e5-a25f-a0baec181b34" />

- Open the windows app and add a new pc.
- Enter in the public IP address for the newly created vm and name it "osticket".
</p>
<br />

<img width="80%" height="80%" alt="5" src="https://github.com/user-attachments/assets/d4524d7b-6e10-471f-b0ea-ffc2270752a9" />

- Click on the osticket vm and enter your username and password that you created when making the virtual machine.
</p>
<br />

<img width="80%" height="80%" alt="6" src="https://github.com/user-attachments/assets/8d12e0ea-f25d-46d0-bb79-cb9906117239" />

- Once you log into the vm open up microsoft edge and lookup this url: https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download
- Download the osTicket instillation file and put the zip folder on your desktop.
- Extract the folder unto the desktop.
</p>
<br />

<img width="80%" height="80%" alt="7" src="https://github.com/user-attachments/assets/2a7ecdbc-c782-4d4d-8d39-f544de5b2146" />

- Open the control panel on the browser.
- Click "uninstall a program" under Programs.
- Click "Turn Windows features on or off" on the left side.
- Check "Internet Information Services" and then expand it.
- Expand "World Wide Web Services".
- Expand "Application Development Features"
- Check "CGI" then press OK and let it install.
</p>
<br />

<img width="80%" height="80%" alt="8" src="https://github.com/user-attachments/assets/7f9490a7-1c30-43ef-b606-e961f65f15e6" />

- Open the osTicket Instillation Files folder you unzipped unto the desktop.
- Click on "PHPManagerForIIS_V1.50" follow all the prompts to install.
</p>
<br />

<img width="80%" height="80%" alt="9" src="https://github.com/user-attachments/assets/7b55ddff-7a74-4b20-9740-b88e44fb0e90" />

- Click "rewrite_amd64_en-US" and follow the prompts to install.
</p>
<br />

<img width="80%" height="80%" alt="10" src="https://github.com/user-attachments/assets/422b09a6-f71c-45ac-b6fa-3bfcead20f10" />

- In File Explorer under "This PC" click "Windows (C:)" and create a new folder titled "PHP"
</p>
<br />

<img width="80%" height="80%" alt="11" src="https://github.com/user-attachments/assets/e80ca45b-d99f-441b-904d-55067b9af77a" />

- Extract the file "php-7.3.8-nts-Win32-VC15-x86" from the "osTicket-Installation-Files" folder into the newly created "PHP" folder on "Windows (C:)".
</p>
<br />

<img width="80%" height="80%" alt="12" src="https://github.com/user-attachments/assets/ad733f9c-b089-4f5d-b098-c15604783dda" />

- From the "osTicket-Intallation-Files" folder click "VC_redist.x86" and follow the prompts to install.
</p>
<br />

<img width="80%" height="80%" alt="13" src="https://github.com/user-attachments/assets/aed5dfbe-ef98-48c4-bdc2-056ff73ab031" />

- From the "osTicket-Installation-Files" folder click "mysql-5.5.62-win32" and follow the prompts to install.
- Once you get to the screen shown in the image up above, choose "Typical" and then next to install.
</p>
<br />

<img width="80%" height="80%" alt="14" src="https://github.com/user-attachments/assets/9843b080-45ac-4ad9-b6f0-02129b5af314" />

- When you get to this screen choose Standard Configuration.
</p>
<br />

<img width="80%" height="80%" alt="15" src="https://github.com/user-attachments/assets/441f9b7b-35ca-41aa-8b56-a0ec4a89fb97" />

- When you get to this screen type "root" for the password.
- Press next and continue the installation until complete.
</p>
<br />

<img width="80%" height="80%" alt="16" src="https://github.com/user-attachments/assets/5f0ccd16-4a63-475a-8fe2-b72349294dad" />

- Click start and type in IIS until you see "Internet Information Services Manager"
- Right click it and run as administrator.
</p>
<br />

<img width="80%" height="80%" alt="17" src="https://github.com/user-attachments/assets/50648646-6c8a-4661-b767-db448b819a4d" />

- Click PHP Manager
</p>
<br />

<img width="80%" height="80%" alt="18" src="https://github.com/user-attachments/assets/322c7309-7841-48bb-a93b-0d6e54b59a5d" />

- Click Register new PHP version.
- Browse to the C drive and click the PHP folder.
- Choose the application "php-cgi"
</p>
<br />

<img width="80%" height="80%" alt="19" src="https://github.com/user-attachments/assets/b6e1fb3a-1b75-499f-b251-f4a23a526c7c" />

- Reload IIS by stopping and restarting the server
</p>
<br />

<img width="80%" height="80%" alt="20" src="https://github.com/user-attachments/assets/4b037931-438a-4e53-b549-7d87abd50a04" />

- Go back to the "osTicket-Installation-Files" folder and extract the files from the folder "osTicket-v1.15.8".
</p>
<br />

<img width="80%" height="80%" alt="21" src="https://github.com/user-attachments/assets/dd83e0ee-61d7-4c03-863c-ab2457ca5e56" />

- From file explore, go to "Windows (C:)", then "inetpub", and then "wwwroot".
- From the "osTicket-v1.15.8" folder you just extracted, drag the "upload" folder into the "wwwroot" folder.
- Rename the "upload" folder to "osTicket".
</p>
<br />

<img width="80%" height="80%" alt="22" src="https://github.com/user-attachments/assets/364c27b7-8d08-4f79-a8cf-fe9608306d17" />

- Once again go to the IIS Manager and stop and restart the server.
</p>
<br />

<img width="80%" height="80%" alt="23" src="https://github.com/user-attachments/assets/9f0d4d07-05e3-4e21-8738-75f759fbf074" />

- In the IIS Manager, on the left side, expand "sites" "Default Web Site" then click on "osTicket".
- On the right side click "Browse".
</p>
<br />

<img width="80%" height="80%" alt="24" src="https://github.com/user-attachments/assets/6644a6aa-4503-47b1-888e-4686126a3048" />

- It should load the osTicket site and look like this.
</p>
<br />

<img width="80%" height="80%" alt="25" src="https://github.com/user-attachments/assets/78084d4f-5419-457e-85a4-959b17135e34" />

- Go back to the IIS Manager and click on osTicket.
- Click PHP Manager.
- At the bottom of the page select "Enable or disable an extenstion"
</p>
<br />

<img width="80%" height="80%" alt="26" src="https://github.com/user-attachments/assets/f14f9a69-0a0a-4773-8a7b-35637f5ef87a" />

- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
</p>
<br />

<img width="80%" height="80%" alt="27" src="https://github.com/user-attachments/assets/52860c8b-3c27-47a9-9848-1b8aff120dfe" />

- osTicket site should look like this now.
</p>
<br />

<img width="80%" height="80%" alt="28" src="https://github.com/user-attachments/assets/6913761f-ca73-4795-859a-144cab93a056" />

- Rename: ost-config.php
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

<img width="80%" height="80%" alt="29" src="https://github.com/user-attachments/assets/3abcbc46-ae81-4a48-861e-cfb1192cf65e" />

- Right click "ost-config.php" and go to properties.
- Click "Security" then click "Advanced".
</p>
<br />

<img width="80%" height="80%" alt="30" src="https://github.com/user-attachments/assets/446e5001-3c4e-48f0-876f-6a0320609d10" />

- Click "Disable inheritance".
- Click "Remove all inherited permissions from this object".
</p>
<br />

<img width="80%" height="80%" alt="31" src="https://github.com/user-attachments/assets/04f22c04-7ea9-4dfc-931f-8aed6f26a348" />

- Click "add" to add new permissions.
- Click "Select a principal"
- Type "everyone"
</p>
<br />

<img width="80%" height="80%" alt="32" src="https://github.com/user-attachments/assets/2ad98eed-91da-424a-bbcc-6fb1e352c3a2" />

- Check "Full control" at this screen then press ok.
</p>
<br />

<img width="80%" height="80%" alt="33" src="https://github.com/user-attachments/assets/4ddc6fec-0b0f-490d-b989-f051099306c9" />

- Click "Apply"
</p>
<br />

<img width="80%" height="80%" alt="34" src="https://github.com/user-attachments/assets/fc19d950-dc81-4355-8d38-7ddb78965830" />

- Go back to this page and click continue.
</p>
<br />

<img width="80%" height="80%" alt="35" src="https://github.com/user-attachments/assets/8efa858d-a8ab-4002-8fa5-e7f4a7aa0bb6" />

- Set up osTicket in the browser by filling in information.
</p>
<br />

<img width="80%" height="80%" alt="36" src="https://github.com/user-attachments/assets/3b22fd13-b37f-4978-ae4b-87e677d08ed1" />

- From the "osTicket-Installation-Files" folder click "HeidiSQL_12.3.0.6589_Setup" and follow the prompts to install.
</p>
<br />

<img width="80%" height="80%" alt="37" src="https://github.com/user-attachments/assets/d81e9fb0-35f0-426b-a28e-8c454b31cefc" />

- Once installation is complete click "New".
- Enter "root" as your password.
</p>
<br />

<img width="80%" height="80%" alt="38" src="https://github.com/user-attachments/assets/12481c8e-94eb-4ead-b66e-60199fe510f2" />

- Right click the "Unnamed" tab, select "create new", and then "database".
</p>
<br />

<img width="80%" height="80%" alt="39" src="https://github.com/user-attachments/assets/44a5e1b2-c777-4914-8de6-be5ecdcbc649" />

- Type in "osTicket" for the name and press ok.
</p>
<br />

<img width="80%" height="80%" alt="40" src="https://github.com/user-attachments/assets/5b035cfe-c8ec-4deb-8e70-987200e3c475" />

- Back to the osTicket installer, fill out the database settings.
- Click install.
</p>
<br />

<img width="80%" height="80%" alt="41" src="https://github.com/user-attachments/assets/b541491e-f800-404c-8b8f-d6d26c6e771d" />

- osTicket should now be installed.
</p>
<br />

<img width="80%" height="80%" alt="42" src="https://github.com/user-attachments/assets/3200d15a-82f6-4e13-8163-957473fe2eec" />

- Browse to your help desk login page: http://localhost/osTicket/scp/login.php
- Login using your username and password.
</p>
<br />
