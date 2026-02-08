# 🧠 My Process 
Step-by-step of how I setup this project. This project is optimized for scalability, meaning it can be used to simulate as many machines as you want. Feel free to make small changes if you want.


# 🕹️ Setting up the Domain Controller
1. Open up Oracle Virtualbox Manager and press new.  
	1. Give your VM a name, and select the .iso file for your server.<br /> <img width="622" height="249" alt="image" src="https://github.com/user-attachments/assets/46b5d876-d0a0-4bf4-ae34-cf7b15713f3b" />
   1. Click on `specify virtual hardware`, and drag the Base Memory to at least 7000mg (7gbs), and select at least 2 CPUs.<br /> *should look something like this* <br /> <img width="620" height="104" alt="image" src="https://github.com/user-attachments/assets/7edd9410-3e6e-4564-b66a-41229f86eaa9" /> 
    1. Also make sure that you have enough storage, I put 40gbs. <br /> <img width="604" height="201" alt="image" src="https://github.com/user-attachments/assets/e14b1eaa-9885-460f-9adb-3b0cb745dbc6" />


2. Open and run your Windows server, select english, and press **Install Now**
   1. Select `Windows Server 2022 Standard Evaluation (Desktop Experience)`
      1. Select Custom Install, and then next. Your windows download will begin so just sit tight. :)
      	1. Once the VM begins rebooting, remove the boot up disk. Then input a password for the Admin.

3. Navigate to `local server` and click on your computer's name.<br /> <img width="612" height="142" alt="image" src="https://github.com/user-attachments/assets/2d130a18-d6ab-4480-b88d-9d736f8ca5a8" /> <br />
   1.  <img width="368" height="42" alt="image" src="https://github.com/user-attachments/assets/363269c8-9023-4eb7-841e-aed9ba97b5b5" /> <--- then select CHANGE in the bottom right 
	1. Change the name of your computer to `AL-DC-01` (AL can be substituted for your state). <br /> <img width="311" height="371" alt="image" src="https://github.com/user-attachments/assets/d209356e-f6f3-4756-be8f-5b625c76e779" />
	 1. Restart your computer to apply the change.

4. 






