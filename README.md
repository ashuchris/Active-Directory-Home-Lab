<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Home Lab – Identity & Access Management</h1>
The objective of this project was to build an Active Directory home lab using Windows Server 2022 and Windows 10 to simulate an enterprise domain environment and perform common IT helpdesk administrative tasks such as user management, access control, and Group Policy configuration.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://youtu.be/hFMQYR5wpyQ)

<h2>Tools and Technologies Used</h2>

- VMware 
- Windows Server 2022
- Windows 10 Enterprise
- Group Policy Objects (GPO)
- Active Directory Domain Services
- DNS
- NTFS File Permissions

<h2>1. Domain Controller Setup</h2>

- Installed Windows Server 2022 using a virtual computer with the VMWare Hypervisor
- Renamed the server to WIN-DC22, gave it a static IP address (192.168.140.128), and changed the DNS server to the server IP
- Added Active Directory Domain Services role
- Promoted the server to the domain controller 

<p>
<img src="https://i.imgur.com/8EIYHbB.png"/>
</p>
<h2>2. Join Windows 10 Client to the domain</h2>

- Installed Windows 10 on the VMware hypervisor
- changed the DNS of the client to the domain controller IP, which was 192.168.140.128 
- Joined the Windows 10 machine to the domain 
<p>
<img src="https://i.imgur.com/H1zRnro.png"/>
</p>

<h2>3. Create Organizational Units, Users, and Security Groups</h2>

- We then create 3 OUs, which are HR, IT, and Sales
- Then create 2 users in each respective OU
- Created 3 security groups, which are HR_Team, Sales_Team and IT_Team, so we assign permissions to a group rather than individually to users.
- Assigned members to those groups we created 

<p>
<img src="https://i.imgur.com/4qtpmTL.png"/>
</p>

<h2>4. Create File Shares and Permissions</h2>

- Created shared folders for each department, which are IT-TOOLs, SALES-REPORT, and HR_FILES
- Then, to make sure only respective departments have access to their files, we assigned NTFS permissions using groups.

<p>
<img src="https://i.imgur.com/tFyWlnw.png"/> <img src="https://i.imgur.com/zonmUSl.png"/>
</p>
<br />
