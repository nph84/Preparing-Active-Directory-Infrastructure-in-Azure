<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Preparing Active Directory Infrastructure in Azure</h1>
This tutorial outlines the environmental preparation of Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)
- 

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/d0f3079d-2794-4bf2-88c0-141fccc7fcd6" height="80%" width="80%" />
</p>
<p>
Create a new resource group to house the virtual machines.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/6ed05a60-8556-4e44-a6cf-015914d9f096" height="10%" width="50%" />
</p>
<p>
Create a virtual network (you can allow Azure to create it automatically as well).
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/31d9ad04-5b67-4943-9f17-420546f6e990" height="80%" width="80%" />
</p>
<p>
Create the virtual machine that will act as the domain controller.
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/ab86b7a4-ca2e-4418-b74e-5a436b969e8e" height="80%" width="80%" />
</p>
<p>
Create a 2nd virtual machine to serve as the client.
</p>
<br />





















