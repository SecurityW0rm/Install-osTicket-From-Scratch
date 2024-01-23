#Install-osTicket-From-Scratch
osTicket client installation on Microsoft Azure

Use the video tutorial and written instructions in conjunction with each other to make the installation easy 



<img width="581" alt="Screenshot 2024-01-16 at 19 23 19" src="https://github.com/chrishernandez9/Install-osTicket-From-Scratch/assets/156137903/e6fc09ad-7448-4fab-b054-2b7a7a96aeda">

Azure ($200 in free credits with a new account): https://azure.microsoft.com/en-us/free/

Video Tutorial: 
[![Install osTicket in Azure]()](https://youtu.be/82hRLTB0-B0)


1. **Create Resource Group**
   - Open the Azure Portal.
   - Create a new resource group named "Lab3RG" with the password "CyberLab123!".

2. **Create Virtual Machine:**
   - Create a virtual machine named "osTicket" in the "USW3" region, running Windows 10 with 4 vCPUs.
   - Use the same username and password throughout the setup.
   - Choose default settings.

3. **Remote Desktop Access:**
   - Obtain the public IP of the "osTicket" VM.
   - Remote Desktop into osTicket using the public IP.

4. **Install IIS with Windows CGI:**
   - (Within VM) Open Control Panel -> Programs -> Turn Windows Features On/Off.
   - Enable Internet Information Services (IIS) with CGI.
   - Test IIS by typing "127.0.0.1" into the browser.

5. **Install Required Components:**
   - Download and install PHP Manager for IIS.
   - Download and install Rewrite Module.
   - Create a "C:\PHP" directory on the local hard drive.

6. **Install PHP 7.3.8:**
   - Download PHP 7.3.8 zip file.
   - Extract files to "C:\PHP".

7. **Install VC_redist:**
   - Install VC_redist from the downloaded files.

8. **Install MySQL Server:**
   - Download and install MySQL Server with standard configuration.
   - Set up credentials: User - root, Password - Password1.

9. **Register PHP in IIS:**
   - Open IIS as an administrator.
   - Register PHP version by browsing to "C:\PHP\php-cgi".
   - Restart the osTicket server in IIS.

10. **Install osTicket:**
    - Copy the contents of the osTicket folder to "C:\inetpub\wwwroot\osTicket".
    - Rename the "upload" folder to "osTicket".
    - Restart IIS.
    - Access the osTicket installer page by browsing to the server.

11. **Configure osTicket:**
    - Enable necessary PHP extensions in PHP Manager.
    - Refresh osTicket installer page.
    - Rename "ost-sampleconfig.php" to "ost-config.php".
    - Set appropriate permissions for "ost-config.php".
    - Continue the setup, providing necessary information.
    - Do not install yet; proceed to install Heidi SQL.

12. **Install Heidi SQL:**
    - Download and install Heidi SQL.
    - Create a new connection with the MySQL credentials (User - root, Password - Password1).

13. **Complete osTicket Setup:**
    - Finish the osTicket setup from the browser.
    - Use MySQL credentials in Heidi SQL.
    - Delete the "setup" folder from "C:\inetpub\wwwroot\osTicket".
    - Adjust permissions for "ost-config.php".
    - Note the login details for future access.


