<h1>Honeypot and SIEM in Azure</h1>


<h2>Description</h2>
ENTER DESCRIPTION OF LAB HERE
<br/>


<h2>Tools and Services Used</h2>

- Azure
- Virtual Machines
- Sentinel
- Log Analytics Workspace
- Powershell
- [ipgeolocation](https://app.ipgeolocation.io/)


<h2>Project Details</h2>

<b>Subscription Details:</b>
- Subscription: Azure subscription 1
- Resource group: honeypot-vm_group

<b>Instance Details:</b>
- Virtual machine name: honeypot-vm
- Region: (US) West US 3
- Availability zone: Zones 1
- Security type: Trusted launch virtual machines
- Image: Windows 10 Pro, version 22h2 - x64 Gen2 (free services available)
- VM Architecture: x64
- Size: Standard_B1s - 1 vCPU, 1 GiB memory

   
<h2>Project walk-through:</h2>

<p align="center">
 #1 
<p align="center">
Create a virutal machine to implement your honeypot.<br/>
<img src="https://i.imgur.com/nu0Hs9A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
 #2 
<p align="center">
Create a Log Analytics Workspace. This will allow us to ingest logs from the Virtual Machine.<br/>
<img src="https://i.imgur.com/DFVr3SB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
 #3 
<p align="center">
We will enable the ability to gather the logs from the Virtual Machine using Microsoft Defender for Cloud. In Environment Settings click on the Log Analytics Workspace that was created in the previous step. Once your in Defender Plans, turn Servers on and save, then in Data collection select All Events and save.<br/>
<img src="https://i.imgur.com/QBdnnHJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
 #4 
<p align="center">
We will now add Microsoft Sentinel. This is the SIEM used to visualize the attack data. Choose your Log Analytics Workspace and Add.<br/>
<img src="https://i.imgur.com/5cm7bFj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p align="center">
 #5 
<p align="center">
Log into your Virtual Machine using Remote Desktop. Turn off the Firewall to make this Virtual Machine vulnerable to outside connections. Make sure to turn the Firewall off in all 3 locations (Domain Profile, Private Profile, Public Profile), <br/>
<img src="https://i.imgur.com/b634SJn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
