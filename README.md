<h1>Active Directory Personal Lab</h1>

 ###

<h2>Description</h2>
Project consists of creating Active Directory Domain Server (AD DS), setting up Remote Access Service (RAS) features to support RAS/NAT, implementing DHCP services and creating client to join to the domain. The client is using dynamic host and connect to the network through domain controller internal network.
The PowerShell script is used to automatically generate more than 1000+ users in active directory based on the user's name. This framework allows you to use any of the created user account in active directory to be able to login to the client PC.
<br />


<h2>Utilities Used</h2>

- <b>VirtualBox</b>
- <b>PowerShell</b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10 Pro (22H2)</b> 

<h2>Lab walk-through:</h2>
<p align="center" width="100%">
 <strong> Project Overview: </strong><br />
 The entire system consists of one Domain Controller and one Client. Client1 will connect to the internet through the internal network to simulate a private network.
 Fully qualified domain name(FQDN) will be set as shiro.com, with the DNS server using the address 172.16.0.1. DHCP IP range for clients is set from 172.16.0.100 to 172.16.0.200. <br />
 <br />
  <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/a84139bd-3e36-48d8-82bb-bdcb093b7a6b" alt="Project Overview"/>
 <br />
 <br />
  Virtual box settings on domain controller: <br />
  Adapter 1 is configured for Internet connection, while Adapter 2 is designated for Internal connectivity. The domain controller for this setup will utilize Windows Server 2019. <br />
  <img width="80%" src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/1058de9f-40e8-430a-ab76-a218337759d6" alt="Virtual Box Settings"/>
  <img width="80%" src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/1565f725-84fe-445a-ab7f-4fb589f546dc" alt="Virtual Box Settings2"/>
 <br />
 <br />
  Within domain controller, configure IP address for the internal network as follows: <br /> 
   <img width="90%" src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/98e31966-d7be-4165-9e5b-4a30bc7efdf8" alt="Set IP Address in DC"/>
 <br />
 <br />
  Next, navigate to the Server Manager, select "Add a new forest", and proceed to create the domain: <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/dfa04a7b-548b-43f6-8a29-a21b4d68a99b" alt="Create Domain"/>
 <br />
 <br />
  Once the domain setup is completed, navigate to Active Directory and proceed to create domain administrators: <br />
   <img width="90%" src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/ddb8d1e7-6e95-42f5-b53a-1cd9aaa7c4bd" alt="Create Admin Account"/>
   <img width="90%" src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/3e3bda98-a3c5-47e3-945e-6d0cc16053a2" alt="Set user as domain admins"/>
 <br />
 <br />
  Return to server manager and initiate the installation of RAS/NAT: <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/88263e6e-9a6b-42fa-bb4a-0fc38af4f7e2" alt="Install RAS"/>
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/8ffc5727-dc7a-40cc-8e6b-c57d4f7e7d5a" alt="Install RAS 2"/>
 <br />
 <br />
  Configure Network Address Translation(NAT) in Routing and Remote Access: <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/be719d97-16f7-4770-909f-263c8fdf0e6e" alt="Configure NAT"/>
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/0a2c5836-a778-44be-871b-8b4faa58850a" alt="Configure NAT 2"/>
 <br />
 <br />
  In Server Manager, proceed to install Dynamic Host Configuration Protocol(DHCP) and configure it with the following IP address range and subnet mask settings: <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/1c2e56aa-c20b-4823-aafb-dff3cc58a14f" alt="Install DHCP"/>
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/173fa1bc-be4c-4c10-9884-285efcdf7496" alt="Install DHCP 2"/>
 <br />
 <br />
   Create a script to automatically generate users in Active Directory. The file names.txt contains over 1000 random user names (First name, Last name): <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/0facf40c-d4ef-4a64-8c58-4c0ffdd923e8" alt="Script to create users"/>
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/244e2268-0e96-436f-92e3-cdecc7198a76" alt="User created"/>
 <br />
 <br />
  Next, create a Windows 10 client with Adapter 1 using Internal connection: <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/2b97a48c-208e-4a34-bec2-98d9965be90b" alt="Creating Client"/>
 <br />
 <br />
  After Windows installation is completed, rename the client to CLIENT1 and join it to the domain 'shiro.com': <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/afda9c40-a4c6-4a3a-914e-51b34e12f4b2" alt="Join Domain"/>
 <br />
 <br />
  Verify IP Configuration from CLIENT1: <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/c179d81f-2af5-43dc-bbe7-a3e9329649d5" alt="IP Config"/>
 <br />
 <br />
  CLIENT1 is successfully receiving address leases, which can be confirmed from the domain controller: <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/891a32e5-af53-407e-89e0-bae0966e425b" alt="Address Leases"/>
 <br />
 <br />
  Client in active directory: <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/052313d1-af9c-40d7-97ee-55e1d22d67e7" alt="Client in Active Directory"/>
 <br />
 <br />
  Any user able to login to the client to simulate the corp environment: <br />
   <img src="https://github.com/shiroma07/ActiveDirectoryLab/assets/44857427/408e72ef-3135-4705-9b03-720f34d244ae" alt="Account login"/>
 <br />
 <br />
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
