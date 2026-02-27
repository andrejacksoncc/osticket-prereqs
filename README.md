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

<img width="80%" height="80%" alt="11" src="https://github.com/user-attachments/assets/e80ca45b-d99f-441b-904d-55067b9af77a" />

- Extract the file "php-7.3.8-nts-Win32-VC15-x86" from the "osTicket-Installation-Files" folder into the newly created "PHP" folder on "Windows (C:)".
</p>
<br />

<img width="80%" height="80%" alt="12" src="https://github.com/user-attachments/assets/ad733f9c-b089-4f5d-b098-c15604783dda" />

- From the "osTicket-Intallation-Files" folder click "VC_redist.x86" and follow the prompts to install.
</p>
<br />
