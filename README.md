<h1>Active Directory Personal Lab</h1>

 ###

<h2>Description</h2>
Project consists of creating Active Directory Domain Server (AD DS), setting up Remote Access Server (RAS) features to support RAS/NAT, implementing DHCP services and creating client to join to the domain. The client is using dynamic host and connect to the network through domain controller internal network.
The PowerShell script is used to automatically generate more than 1000+ users in active directory based on the user's name. This framework allows you to use any of the created user account in active directory to be able to login to the client PC.
<br />


<h2>Utilities Used</h2>

- <b>VirtualBox</b>
- <b>PowerShell</b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10 Pro (22H2)</b> 

<h2>Lab walk-through:</h2>
<p align="center">Virtual box settings on DC: <br />

<img align="left" width="100" height="100" src=![Virtual Box Settings](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/1058de9f-40e8-430a-ab76-a218337759d6)>
![Virtual Box Settings2](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/1565f725-84fe-445a-ab7f-4fb589f546dc)

<br />

<p align="center">Set IP address for internal network: <br />
 
  ![Set IP Address in DC](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/98e31966-d7be-4165-9e5b-4a30bc7efdf8)

<p align="center">Creating domain in domain controller: <br />

  ![Create Domain](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/dfa04a7b-548b-43f6-8a29-a21b4d68a99b)

<p align="center">Creating admin account in active directory: <br />

  ![Create Admin Account](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/ddb8d1e7-6e95-42f5-b53a-1cd9aaa7c4bd)
  ![Set user as domain admins](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/3e3bda98-a3c5-47e3-945e-6d0cc16053a2)

<p align="center">Installing RAS/NAT: <br />

   ![Install RAS](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/88263e6e-9a6b-42fa-bb4a-0fc38af4f7e2)
   ![Install RAS 2](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/8ffc5727-dc7a-40cc-8e6b-c57d4f7e7d5a)

<p align="center">Configuring NAT: <br />

  ![Configure NAT](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/be719d97-16f7-4770-909f-263c8fdf0e6e)
  ![Configure NAT 2](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/0a2c5836-a778-44be-871b-8b4faa58850a)

<p align="center">Install DHCP: <br />

   ![Install DHCP](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/1c2e56aa-c20b-4823-aafb-dff3cc58a14f)
   ![Install DHCP 2](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/173fa1bc-be4c-4c10-9884-285efcdf7496)

 <p align="center">Script to create users: <br />
  
   ![Script to create users](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/0facf40c-d4ef-4a64-8c58-4c0ffdd923e8)
   ![User created](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/244e2268-0e96-436f-92e3-cdecc7198a76)



 
<p align="center">Create : <br />
 
<p align="center">Client join to the domain created in domain controller: <br />
 
![Join Domain](https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/afda9c40-a4c6-4a3a-914e-51b34e12f4b2)
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
