<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory and adding and Admin Account within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Install Active Directory
- Create Domain Admin
- Join Client to Domain


<h2>Deployment and Configuration Steps</h2>

![Screenshot (17)](https://github.com/user-attachments/assets/e55731d4-aa9e-4b7e-b9cd-c81454d4ca35) ![Screenshot (18)](https://github.com/user-attachments/assets/ad423f83-a59a-4102-8eb5-fab0af51033f)



<p>
To install Active Directory, I began by launching Server Manager on my Windows Server. From there, I navigated to the "Add Roles and Features" section, selected Active Directory Domain Services (AD DS) as the role, and proceeded with the installation.  I subsequently promoted the server to function as a domain controller and proceeded to establish a new forest within the server.
</p>
<br />

![Screenshot (21)](https://github.com/user-attachments/assets/60dd7f3a-dc44-4995-a604-9a823a7dd8c6) ![Screenshot (23)](https://github.com/user-attachments/assets/37ba07e0-ed56-43cb-b70c-aa5de988b4f9)


<p>
I created a new Organizational Unit (OU) titled "_ADMINS" and within it, provisioned a new user account for an employee named "Jane Doe," with the username "jane_admin." I then assigned "jane_admin" to the "Domain Admins" security group, granting her elevated administrative privileges within the domain.
</p>
<br />

![Screenshot (25)](https://github.com/user-attachments/assets/06d19ba8-3f23-4bd7-a49d-abf1c8013e5f)

<p>
Using the Azure portal, I configured the client's DNS settings to point to the server's private IP address, facilitating the client's connection to the server.
</p>
<br />
