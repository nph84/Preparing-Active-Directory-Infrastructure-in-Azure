<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Preparing Active Directory Infrastructure in Azure</h1>
This tutorial outlines the environmental preparation of Active Directory within Azure virtual machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Set up a domain controller in Microsoft Azure
- Set up a client PC in Microsoft Azure

<h2>Deployment and Configuration Steps</h2>

<p>
Create a new resource group to house the virtual machines. <br /> <br />
<img src="https://github.com/user-attachments/assets/d0f3079d-2794-4bf2-88c0-141fccc7fcd6" height="80%" width="80%" />
</p>
<br />


<p>
Create a virtual network (you can also allow Azure to create it automatically). <br /> <br />
<img src="https://github.com/user-attachments/assets/6ed05a60-8556-4e44-a6cf-015914d9f096" height="10%" width="50%" />
</p>
<br />



<p>
Create the virtual machine that will act as the domain controller. <br /> <br />
<img src="https://github.com/user-attachments/assets/31d9ad04-5b67-4943-9f17-420546f6e990" height="80%" width="80%" />
</p>
<br />



<p>
Create a 2nd virtual machine to serve as the client. <br /> <br />
<img src="https://github.com/user-attachments/assets/ab86b7a4-ca2e-4418-b74e-5a436b969e8e" height="80%" width="80%" />
</p>
<br />



<p>
Back on Microsoft Azure, set the domain controller's NIC private IP address to be static. <br /> <br />
<img src="https://github.com/user-attachments/assets/3db68ba4-9606-413a-9353-ef048f9c5674" height="80%" width="80%" /> <br /> <br />
<img src="https://github.com/user-attachments/assets/bf9686d9-a35d-4139-8aaa-f7df31102263" height="80%" width="80%" />
</p>
<br />


<p>
Inside of RDP on the domain controller virtual machine, we'll disable Windows firewall for checking connectivity. We will do this by right-clicking on the start button and clicking "run". After doing that, we will type "wf.msc". <br /> <br />
<img src="https://github.com/user-attachments/assets/7e7f5043-4921-43b6-97ae-8ecddfcdbeb7" height="80%" width="80%" />
</p>
<br />


<p>
Return to Microsoft Azure and set the client virtual machine's DNS settings to the domain controller vm's private IP address. <br /> <br />
<img src="https://github.com/user-attachments/assets/f96b1a19-a5f6-4a8b-9e18-64ac9c0cafbc" height="80%" width="80%" /> <br /> <br />
<img src="https://github.com/user-attachments/assets/c0fd3d25-d2bd-4bbe-982b-b1ead1c163fe" height="80%" width="80%" /> <br /> <br />
</p>
<br />



<p>
After logging back into the client virtual machine, open PowerShell, and we will ping the domain controller's IP address. <br /> <br />
<img src="https://github.com/user-attachments/assets/c2c5beec-ddbb-4331-9a22-ef8cacf7d787" height="80%" width="80%" />
</p>
<br />



<p>
Next, type ipconig /all in PowerShell, and it should show the domain controller's IP settings. <br /> <br />
<img src="https://github.com/user-attachments/assets/7fcbe3bf-b959-43f6-8c7a-07d0edad5cb5" height="80%" width="80%" />
</p>
<br />





















