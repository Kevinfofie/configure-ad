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

- Step 1 Creating the Domain Controller and client in  Microsoft Azure (Virtual Machines, Windows Server 2022) named “DC-lab”

- Step 2 Install Active Directory

- Step 3 Creating an Admin and Normal User Account in AD-lab

- Step 4 Join Client to your domain (fofie.com)

- Step 5 Setup Remote Desktop for non-administrative users on Client
- Step 6 Create a bunch of additional users and attempt to log into client-1 with one of the users


<h2>Deployment and Configuration Steps</h2>

Step 1 Creating the Domain Controller and client in  Microsoft Azure (Virtual Machines, Windows Server 2022) named “DC-lab”
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
Step 2 Installation of Active Directory
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
After a sucessful login to DC-lab, we install Active Directory Domain Services, next we Promote as a DC: Seting up a new forest as fofie.com.
</p>
Step 3 Creating an Admin and Normal User Account in AD-lab
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
