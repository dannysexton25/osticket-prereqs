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

- Item PHP Manager for IIS
- Item Rewrite Module
- Item PHP 7.3.8
- Item VC_redist.x86.exe
- Item MySQL 5.5.62
- Item HeidiSQL
- Item osTicket-v1.15.8.zip

## Installation Steps:

## 1. Install / Enable IIS in Windows with CGI 



<img src="https://github.com/user-attachments/assets/928bf796-15c7-493b-ba20-35ee05ce3cb2" width="325" height="250"><img src="https://github.com/user-attachments/assets/b5e90ae2-7853-42b7-b190-138c3eac8c76" width="325" height="250"><img src="https://github.com/user-attachments/assets/a343f202-6651-4758-ab9f-32e94c4e309e" width="325" height="250">

  ### 📋Installation Instructions

  1. **Open the Control Panel** 
 
   Go to the **Start** menu, type **Control Panel** in the search bar, and open it.

2. **Access Programs and Features**  
   Under **Programs**,click **Uninstall a program**.

3. **Enable Internet Information Services (IIS)**  
   On the left, click **Turn Windows features on or off**.  
   Check the box for **Internet Information Services**.

4. **Expand Required Sections**  
   - Expand **Internet Information Services**
   - Expand **World Wide Web Services**
   - Expand **Application Development Features**

5. **Enable CGI**  
   Check the box for **CGI**, then click **OK** to apply the changes.

> 💡 *Note: All required areas have been highlighted for your convenience.*

## 2. Download and Install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

<img src="https://github.com/user-attachments/assets/b5639352-dd84-410b-89ba-6d554272cb4b" width="325" height="250"><img src="https://github.com/user-attachments/assets/a1ae1aaf-a508-4eec-a4c4-b1edcf5a7bb2" width="325" height="250"><img src="https://github.com/user-attachments/assets/6d1a6bff-267c-47f9-ab35-3dca2397feda" width="325" height="250">
### 🛠️ PHP Manager for IIS Installation

1. Open **PHPManagerForIIS-V1.5.0**.
2. Click **Next** to begin the installation.
3. Accept the license agreement by selecting **I Agree**, then click **Next** to continue.
> 💡 *Note: All required areas have been highlighted for your convenience.*
## 3. Download and Install the Rewrite Module (rewrite_amd64_en-US.msi)

<img src="https://github.com/user-attachments/assets/111d2b62-980b-4087-86c5-9a9097671bdd" width="325" height="250">
<img src="https://github.com/user-attachments/assets/e80d0861-f975-4e09-b5bb-7bfac015f960" width="325" height="250">
<img src="https://github.com/user-attachments/assets/bbba7b0f-7ceb-43e6-a12e-9881b648c6ac" width="325" height="250">
 
 ### 📋Installation Instructions
1. **Download the Installer**  
   Click to download `rewrite_amd64_en-US.msi` from the official Microsoft site.

2. **Launch the Installer**  
   Double-click the downloaded `.msi` file to begin installation. Click **Next** on the setup wizard.

3. **Accept the License Agreement**  
   Select **I Agree**, then click **Install** to begin the installation.
> 💡 *Note: All required areas have been highlighted for your convenience.*
## 4. Create a Directory for PHP on the local hard drive.

<img src="https://github.com/user-attachments/assets/91fa0138-72d8-4073-873f-e418152114d2" width="325" height="250">
<img src="https://github.com/user-attachments/assets/0e776c63-a7f7-4ca9-9c7a-070ac9d95401" width="325" height="250">
<img src="https://github.com/user-attachments/assets/b359c1ff-58a7-4c75-b2dc-bb5daef1977e" width="325" height="250">
 
 ### 📋Installation Instructions
1. **Open File Explorer**  
   Navigate to the local disk where you want to install PHP (usually `C:\`).

2. **Create a New Folder**  
   Right-click in the desired location and select **New > Folder**.

3. **Name the Folder `PHP`**  
   Type `PHP` as the folder name and press **Enter**.
> 💡 *Note: All required areas have been highlighted for your convenience.*
> ✅ *Tip: This folder will be used later to store PHP runtime files.*

## 5. Download the PHP zip package and extract it into the `C:\PHP` folder you created earlier. 
<img src="https://github.com/user-attachments/assets/cfb2ac8d-ace3-4564-b84b-253399dadb52" width="325" height="250">
<img src="https://github.com/user-attachments/assets/c9039356-4033-42db-9d40-b28b4077e379" width="325" height="250">
<img src="https://github.com/user-attachments/assets/ca1e6690-0e95-4e67-92f0-520d749e96a8" width="325" height="250">
<img src="https://github.com/user-attachments/assets/73907091-e1a7-44c7-8dc6-e400ca637f9c" width="325" height="250">
<img src="https://github.com/user-attachments/assets/3f52dc6b-c17e-40cf-9487-5491956bb833" width="325" height="250">
<img src="https://github.com/user-attachments/assets/6e9a41e3-adac-4646-a795-3c080f76a773" width="325" height="250">

 ### 📋Installation Instructions

1. **Download PHP 7.3.8**  
   Go to the PHP download page and get the file:  
   `php-7.3.8-nts-Win32-VC15-x86.zip`

2. **Open the Download Location**  
   After the download finishes, go to your Downloads folder.

3. **Extract the ZIP File**  
   Right-click the downloaded zip file and choose **Extract All...**

   4. **Choose the Destination Folder**  
   In the extract window, set the location to `C:\PHP`.
> 💡 *Note: You can either browse to the location manually or simply type C:\PHP into the box.*
 5. **Start the Extraction**  
   Click **Extract** to begin unzipping the files.

  6. **Verify the Files**  
   Once finished, open `C:\PHP` and confirm the PHP files are there.
> 💡 *Note: All required areas have been highlighted for your convenience.*
> ✅ *You now have PHP 7.3.8 ready to configure in IIS!*

## 6. Download and Install VC_redist.x86.exe.
<img src="https://github.com/user-attachments/assets/135e1417-946a-47b2-baad-b394c8d65e65" width="325" height="250">
<img src="https://github.com/user-attachments/assets/5e8d4fa3-c6c4-483c-a1c9-ffe32c30e127" width="325" height="250">
<img src="https://github.com/user-attachments/assets/25a2489b-abd2-4c54-bf51-1e3844751b1c" width="325" height="250">
## 6. Download and Install VC_redist.x86.exe

This step installs the **Visual C++ Redistributable**, which is required for PHP to run.
 ### 📋Installation Instructions
1. **Download the Installer**  
   Go to the official Microsoft website and download `VC_redist.x86.exe`.

2. **Run the Installer**  
   Once downloaded, double-click the file to launch the installer.
3. **Accept and Install**  
   - Check the box to agree to the license terms  
   - Click **Install** to begin the installation
> 💡 *Note: All required areas have been highlighted for your convenience.*
> ✅ *Once the installation completes, you're ready for the next step!*
## 7. Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi).



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
