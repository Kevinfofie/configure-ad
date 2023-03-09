# configure-ad<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1 Creating the Domain Controller and client in  Microsoft Azure (Virtual Machines, Windows Server 2022) named “DC-lab”.

- Step 2 Install Active Directory.

- Step 3 Creating an Admin and Normal User Account in AD-lab.

- Step 4 Join Client to domain (fofie.com).

- Step 5 Setup Remote Desktop for non-administrative users on Client.
- Step 6 Creating and adding users using PowerShell_ise and logging into client with one of the newly ctreated users.


<h2>Deployment and Configuration Steps</h2>

Step 1 Creating the Domain Controller and client in  Microsoft Azure (Virtual Machines, Windows Server 2022) named “DC-lab”.
<br />

<p>
<img src="https://i.imgur.com/SSbqS4w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/20NbFKW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/s6yAeka.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/ELsUDvG.pngg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Creation of damain controller.
</p>
<br />
<p>
<img src="https://i.imgur.com/bTWGHSl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/74fMrN3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Creation of client VM with user name "labuser".
</p>
Step 2 Installation of Active Directory.
</p>
<br />

<p>
<img src="https://i.imgur.com/IF8Ueze.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/3GOElfa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/ymSrDkl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/kTLgMg8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/QoISSPw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/oJIl4Uu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/V3WsJe3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After a successful login to DC-lab, we install Active Directory Domain Services fofie.com.
</p>
Step 3 Creating an Admin and Normal User Account in AD-lab.
</p>
<br />
<p>
<img src="https://i.imgur.com/TD5vfpW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/juqX8FI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/gbfNRe4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/jglq0Pz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After the creation of domain controllers, next we Promote as a DC: Seting up a new forest as fofie.com. In Active Directory Users and Computers (ADUC), creating an Organizational Unit (OU) called “_EMPLOYEES”. Additionally, Creating a new Organizational Unit (OU) named “_ADMINS” Furthermore, we add a new administrator into the system as Adam Doe, with the username adam_admin log out and sign in as an admin called adam_admin.
</p>
<p>
<img src="https://i.imgur.com/9RAhMtQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/1AerEZl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After logging off, we sign in as one of the administrators adam_admin.
</p>
Step 4 Adding  Client to domain (fofie.com) from the Azure Portal.
</p>

<br />
<p>
<img src="https://i.imgur.com/9vveeSA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/xKuVI4z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Azure Portal, we set Client’s DNS settings to the DC’s Private IP address and from the Azure Portal, we restart Client.
</p>
<img src="https://i.imgur.com/yWffgdW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

First we Loggin to the Domain Controller (Remote Desktop) and verifying that Client shows up in Active Directory Users and Computers (ADUC).
</p>
<br />
<p>
Logging in to Client (Remote Desktop) as the original local admin (labuser) and joining it to the domain fofie.com (computer will restart).
</p>
<img src="https://i.imgur.com/pBaP2wi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/YIaFIP1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/rbwkoAI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 5 Setup Remote Desktop for non-administrative users on Client.
<br />
Setting up Remote Desktop for non-administrative users on Client, we Log into Client as fofie.com\adam_admin and open system properties Click “Remote Desktop” Allow “domain users” access to remote desktop. Afterwards we can now log into Client as a normal non-administrative user.
</p>
<img src="https://i.imgur.com/A39hNpF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Step 6 Creating and adding users using PowerShell_ise and logging into client with one of the newly ctreated users.
</p>
<br />

<img src="https://i.imgur.com/Kb9euqE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/5sS2mCN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Logging into DC-lab as adam_admin and Opening PowerShell_ise as an administrator. Runing the script and observing the accounts being created.
</p>
<img src="https://i.imgur.com/QYxabZu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Accounts successfully created.
</p>
<br />
Opening Active Directory users and computers on DC-lab and  observing if the newly created accounts are in the appropriate Organisation Units.
</p>
<img src="https://i.imgur.com/ZUCq0NJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Finally logging in to client as a normal user.
</p>
<img src="https://i.imgur.com/uUwvCMw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/FBufUQi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Successfully creating and logging in a normal user who can login to the system and perform some tasks.
</p>

