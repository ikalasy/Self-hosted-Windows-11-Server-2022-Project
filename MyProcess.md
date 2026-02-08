# 🧠 My Process 
Complete guide to setting this project. This guide will walk you through how to setup a Domain Controller, Active Directory, Roles and Permissions, Intune, implement Patch Management, Join a machine to a domain, and NTFS through virtualization.
There are many ways to do this, and can be done on a level 1 Hypervisor instead of Virtualbox ex. Proxmox.  

What I want from this project:  

	-Full functioning Domain Controller VM, and a user VM on the same subnet.  
	
	-Active Directory, and forest setup within the subnet. 
	
	-Multiple user accounts, each with their own grouping based off of their role. (Security, Sales, Tech, Etc.) 
	
	-Network drives with strict permission access.   
	
	-A ticketing system.  
	
	-Scalability (So that more user VMs can be installed, simulating a larger user base)  
	
	-To implement a patch manager for the DC and User systems.  

	-To perform tasks as if I was a Help Desk technician, resetting passwords, unlocking user accounts, changing group policy, disabling accounts, etc.
	
	


# 🕹️ Setting up the Domain Controller
1. Open up Oracle Virtualbox Manager and press new.  
	1. Give your VM a name, and select the .iso file for your server.<br /> <img width="622" height="249" alt="image" src="https://github.com/user-attachments/assets/46b5d876-d0a0-4bf4-ae34-cf7b15713f3b" />
   1. Click on `specify virtual hardware`, and drag the Base Memory to at least 7000mg (7gbs), and select at least 2 CPUs.<br /> *should look something like this* <br /> <img width="620" height="104" alt="image" src="https://github.com/user-attachments/assets/7edd9410-3e6e-4564-b66a-41229f86eaa9" /> 
    1. Also make sure that you have enough storage, I put 40gbs. <br /> <img width="604" height="201" alt="image" src="https://github.com/user-attachments/assets/e14b1eaa-9885-460f-9adb-3b0cb745dbc6" />


2. Open and run your Windows server, select english, and press **Install Now**
   1. Select `Windows Server 2022 Standard Evaluation (Desktop Experience)`
      1. Select Custom Install, and then next. Your windows download will begin so just sit tight. :)
      	1. Once the VM begins rebooting, remove the boot up disk. Then input a password for the Admin.

3. Rename your computer. 
   1. Navigate to `local server` and click on your computer's name.<br /> <img width="612" height="142" alt="image" src="https://github.com/user-attachments/assets/2d130a18-d6ab-4480-b88d-9d736f8ca5a8" /> <br />
    1.  <img width="368" height="42" alt="image" src="https://github.com/user-attachments/assets/363269c8-9023-4eb7-841e-aed9ba97b5b5" /> <--- then select CHANGE in the bottom right 
	 1. Change the name of your computer to `AL-DC-01` (AL can be substituted for your state). <br /> <img width="311" height="371" alt="image" src="https://github.com/user-attachments/assets/d209356e-f6f3-4756-be8f-5b625c76e779" />
	  1. Restart your computer to apply the change.

5. Install Active Directory  
   1. Select manage -> add roles and features -> press next until you get to Server Roles
    1. Select Active Directory Domain Services, and thenn press Add Features. <br /> <img width="692" height="465" alt="image" src="https://github.com/user-attachments/assets/75585241-5f55-4f02-89d0-9ec405db2c1e" />
     1. Press next and then press install on the final page, and wait for it to finish installing.
  
coffee break... ☕

6. Promote your computer to a Domain Controller
   1. Click on the flag with a caution sign in the top left, and then on `Promote this server to a Domain Controller`
    1. Select `Add a new forest`, and then input your custom domain name. <br /> <img width="420" height="160" alt="image" src="https://github.com/user-attachments/assets/fab35437-f22b-4f33-a138-f61d5a352db3" />
	 1. On the next page input your Administrator password and hit next until you're prompted to install, and then start to apply changes.

7. Install guest addition on your Domain Controller
   1. Select devices at the top of the VM window and select `inset guest additions`
    1. Open file explorer and navigate to `CD Drive (D:)VirtualBox`
     1. Install `VBoxWindowsAdditions-arm64` <br /> <img width="603" height="111" alt="image" src="https://github.com/user-attachments/assets/8df4bebb-158c-4837-83a3-f52457560667" />











