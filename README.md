<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Precursor to Security Operations Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of failed auth and log observations within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy Security Operations within Azure Compute](https://youtu.be/cG7M3Z-Cek4)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup resources in Azure
- Ensure connectivity between Client-1 and Domain Controller (DC-1)
- Installing Active Directory
- Creating an Admin and Normal User account in AD
- Join Client-1 to your domain
- Setup Remote Desktop (RDP) for non-admin users on Client-1
- Create a bunch of additional users and attempt to log into Client-1 with one of the users

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="" height="80%" width="80%""/>


</p>
<p>
Diagram
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/1cd8269e-3e8b-49ae-97b8-9a3e5d2c3b2e" height="80%" width="80%""/>

</p>
<p>
Created a new VM called 'Cat-Attack-vm' with a resource group called 'Cyber-Cat-Attack-RG' and a Virtual Network called 'VNet-Cat-Attack'. 
  Since we are going to be attacking this vm, we set the current location to Southeast Asia to see what an attack would 
  look like coming from an outside source.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/a9614074-9471-4a52-ad10-51f1e6d0cc1d" height="80%" width="80%""/>
<img src="https://github.com/user-attachments/assets/1450f214-d036-4820-84c9-1b3210076069" height="80%" width="80%""/>


</p>
<p>
Remote Desktop into Windows-vm and attempted to login. Attempt failed exactly like we wanted.
</p>
<br />

<p>
  <img src="https://github.com/user-attachments/assets/f9398be7-ba1c-4a89-a34b-2215ced9834f" height="80%" width="80%""/>
  <img src="https://github.com/user-attachments/assets/17ccb149-1dc0-4ada-b4b4-a00573ed5ad2" height="80%" width="80%""/>
  <img src="https://github.com/user-attachments/assets/5b342db6-d75d-4620-9d58-adb8b3249529" height="80%" width="80%"" />
  <img src="https://github.com/user-attachments/assets/6e499f85-4375-4dca-aa8b-230e66d2522f" height="80%" width="80%"" />

</p>

<p>
  Downloaded SSMS unto Cat-Attack-vm and attempt to login with Windows-vm server, Login username & password.
</p>
<br />


<p>
  <img src="https://github.com/user-attachments/assets/8c0e70ee-ed79-4ed5-9b77-5676d2bc8f75" height=80%" width="80%""/>
  

</p>
 
  
<p>
Was able to generate some failed SSH logs against Linux-vm.
</p>

<br />
