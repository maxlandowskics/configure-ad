# configure-ad<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Create a new Azure Active Directory tenant
- Step 2: Create a new Azure Virtual Network
- Step 3: Deploy a Windows Server Virtual Machine
- Step 4: Configure Active Directory Domain Services (AD DS)
- Step 5: Verify the Active Directory Deployment

<h2>Step 1: Create a new Azure Active Directory tenant</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Sign in to the Azure portal (portal.azure.com).
In the left-hand menu, click on "Azure Active Directory."
Click on "Create a tenant" and follow the prompts to create a new Azure Active Directory tenant.
Note down the Directory ID, as you'll need it later.
</p>
<br />
<h2>Step 2: Create a new Azure Virtual Network</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the Azure portal, navigate to "Virtual networks" and click on "Create a virtual network."
Provide a name for the virtual network and select the desired configuration options.
Configure the address space and subnet for the virtual network.
Click on "Review + Create" and then "Create" to create the virtual network.
</p>
<br />
<h2>Step 3: Deploy a Windows Server Virtual Machine</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the Azure portal, navigate to "Virtual machines" and click on "Add."
Provide the necessary details for the virtual machine, such as name, region, and resource group.
Select the appropriate image for the Windows Server OS.
Choose the desired size and configuration options for the virtual machine.
Configure the networking settings, including the virtual network created in Step 2.
Provide administrative credentials for the virtual machine.
Review the settings and click on "Review + Create" and then "Create" to deploy the virtual machine.
</p>
<br />
<h2>Step 4: Configure Active Directory Domain Services (AD DS)</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the virtual machine is deployed, navigate to its overview page in the Azure portal.
Click on "Connect" to establish a remote desktop connection to the virtual machine.
Log in to the virtual machine using the administrative credentials provided during deployment.
In Server Manager, click on "Add roles and features" and follow the wizard to install the Active Directory Domain Services role.
After the role installation completes, open "Server Manager" and click on "Promote this server to a domain controller."
In the Active Directory Domain Services Configuration Wizard, select "Add a new forest" and provide a root domain name.
Set the Forest Functional Level and Domain Functional Level based on your requirements.
Configure the desired Directory Services Restore Mode (DSRM) password.
Specify the DNS options and leave other settings as default.
Review the settings and click on "Install" to promote the server to a domain controller.
  </p>
<br />
<h2>Step 5: Verify the Active Directory Deployment</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Once the promotion process completes, restart the virtual machine.
After the restart, log in to the domain controller using the domain administrator credentials.
Open "Server Manager" and navigate to "Tools" > "Active Directory Users and Computers" to verify the Active Directory deployment.
You can create users, groups, and organizational units to start managing your Active Directory environment.
  </p>
<br />
Congratulations! You have successfully deployed Active Directory on Azure cloud. You can now manage user accounts, security policies, and group policies using the Azure Active Directory service. Remember to properly secure and manage your Active Directory environment to ensure the integrity and security of your organization's resources.
Congratulations! You have successfully deployed Active Directory on Azure cloud. You can now manage user accounts, security policies, and group policies using the Azure Active Directory service. Remember to properly secure and manage your Active Directory environment to ensure the integrity and security of your organization's resources.
