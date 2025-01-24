<H1>Overview: LAB2 Getting Started with Active Directory</H1>

Welcome to the second lab in my home lab series! This section of my home lab documents the process of **Changing our Server Name** and setting up a **Active Directory** in our server. It outlines the steps for renaming the server to a more recognizable name **DC01**, followed by installing **Active Directory Domain Services** role. In the process we will promote our server to be a domain controller. This task serves as the foundation for building proficiency in user account management with Active Directory.
<H2>Objectives</H2>

This repository documents a comprehensive home lab project focused on installing and configuring Active Directory Domain Services. The key objectives include:

- Renaming our server to a recognizable name; DC01.
- Installing Active Directory Domain Services Role

<H2>Documentation</H2>

This lab shows a step-by-step procedure of renaming our server, the we will install Active Directory Domain Services and promote our server to act as a domain controller.
To begin we will login to our server and navigate to "Windows Explorer" and then to "This PC" icon. Right click on it and choose the "Properties" option at the bottom of the menu options. This will open the "About" page of our computer.

1.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%20One.png?raw=true" width="400px"/>
   <br />
   <br />

   
As you can see, the current name of the computer is quite hard to recognize, so to change this click on the "Rename this PC" box and proceed to input a preferred name. We will name it DC01 to identify our server as our domain controller.


2.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%20Two.png?raw=true" width="400px"/>
   <br />
   <br />
Click "Next" and the restart the virtual computer for the changes to take place. 


3. 
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%20Three.png?raw=true" width="400px"/>
   <br />
   <br />

   
4. 
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%20Four.png?raw=true" width="400px"/>
   <br />
   <br />
Now we can confirm that the name of our computer has changed to "DC01".


5. 
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%20Five.png?raw=true" width="400px"/>
   <br />
   <br />
The next step, we will assign a static IP Address to our server before we promote it to act as a domain controller. This will enable us to join other computers our domain and we need an IP Address to refer to and leaving the "DCHP" settings on will keep changing the IP Address.
To do this, open "Network & Internet" settings, then click on "Change Adapter Settings". Once, on the next page right-click on "Ethernet" and the click on "Properties" to open the IP configuration console.


6. 
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%206.png?raw=true" width="400px"/>
   <br />
   <br />

   
7. 
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%207.png?raw=true" width="400px"/>
   <br />
   <br />

   
8. 
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%208.png?raw=true" width="400px"/>
   <br />
   <br />

      
Disable "IPv6" since we are using IPV4 by unchecking the box. Then click on "IPv4" and choose "Properties" and click "OK".


9. 
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%209.png?raw=true" width="400px"/>
   <br />
   <br />
   
Let's check the current network configuration information by running "ipconfig" on command prompt. We have to run command prompt as a "Administrator" to get the rights.

10.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%2010.png?raw=true" width="400px"/>
   <br />
   <br />

11.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%2011.png?raw=true" width="400px"/>
   <br />
   <br />
   
Check the "Use the following IP Address" then input the above information. We will use our primary IP Address "10.0.2.15"as the "Preferred DNS server" as later on, we will use it as a DNS server. Then click "OK" in this page and the next one to save the changes.


12.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%2012.png?raw=true" width="400px"/>
   <br />
   <br />

   
Next, we will install Active Directory role on our Server2022. Open Server Manager, click on "Manage" in the top right corner, then select "Add Roles and Features." Click "Next," then choose "Role-based or feature-based installation" and click "Next" again to proceed.


13.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%2013.png?raw=true" width="400px"/>
   <br />
   <br />

   
Click "Next"

14.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%2014.png?raw=true" width="400px"/>
   <br />
   <br />
   
Select the name of your computer and click "Next"


15.
  
  <p align="center">
  <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%2015.png?raw=true" width="400px"/>
  <br />
  <br />
Select "Active Directory Domain Services," then click "Add Features" when prompted. After that, click "Next" to continue.

     
16.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step%2016.png?raw=true" width="400px"/>
   <br />
   <br />

   
17.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step32.PNG?raw=true" width="400px"/>
   <br />
   <br />
   
Click "Next"


18.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step17.png?raw=true" width="400px" />
   <br />
   <br />

   
20.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step18.png?raw=true" width="400px"/>
   <br />
   <br />
   

Finally select “Install”.

21.
 
  <p align="center">
  <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step19.png?raw=true" width="400px"/>
  <br />
  <br />

Once the installation is complete, select “Promote this server to a domain controller” option. This configures our server to a domain controller.

22.
  
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step20.png?raw=true" width="400px"/>
   <br />
   <br />
   
Incase you click "Close" you can still find the link under "Tasks" tab at the top.

      
23.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step21.png?raw=true" width="400px"/>
   <br />
   <br />
   
Select "Add a new forest" and enter your preferred domain name and it should be in the form of "******.com". We will use "junicetechie.com" as our root domain name. Then click "Next" to proceed.


24.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step22.png?raw=true" width="400px"/>
   <br />
   <br />

Create a password for our Directory Service Restore Mode (DSRM) then click “Next”. 

25.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step23.png?raw=true" width="400px"/>
   <br />
   <br />

Click “Next” then “Install”.


26.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step24.png?raw=true" width="400px"/>
   <br />
   <br />
   
NetBIOS name is auto-filled. Click "Next" to proceed.

27.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step25.png?raw=true" width="400px"/>
   <br />
   <br />

   
28.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step26.png?raw=true" width="400px"/>
   <br />
   <br />

   
29.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step27.png?raw=true" width="400px"/>
   <br />
   <br />

   
All prerequisite checks have passed and we are ready to install. Click "Install" button to begin installation.


28.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step28.png?raw=true" width="400px"/>
   <br />
   <br />

After installation of Active Directory Domain Services is complete, the virtual machine will restart. Once the restart is complete, sign back in by selecting "Input" and clicking the "Ctrl + Alt + Del" button. You will notice that the login page has changed showing "JUNICETECHIE\Administrator." This confirms that the installation and domain controller promotion was successful.Go ahead and sign in to your account using the admin credentials to login in to our domain controller.


30.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step30.png?raw=true" width="400px"/>
   <br />
   <br />
We can confirm that we are in the domain that we set earlier.


31. 
   
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Active-Directory-Domain-Services/blob/main/Files/Step31.png?raw=true" width="400px"/>
   <br />
   <br />

Well done!!We have successfully configured a domain controller "junicetechie.com" with Active Directory installed!! 


 👉 [Next Lab 3 : Active Directory Account Creation, CMD Commands](https://github.com/Simokid/Active-Directory-Account-Creation-CMD-Commands)








