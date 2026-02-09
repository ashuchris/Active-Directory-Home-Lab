<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Home Lab – Identity & Access Management</h1>
The objective of this project was to build an Active Directory home lab using Windows Server 2022 and Windows 10 to simulate an enterprise domain environment and perform common IT helpdesk administrative tasks such as user management, access control, and Group Policy configuration.<br />


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

</br>
<h2>2. Join Windows 10 Client to the domain</h2>

- Installed Windows 10 on the VMware hypervisor
- changed the DNS of the client to the domain controller IP, which was 192.168.140.128 
- Joined the Windows 10 machine to the domain 
<p>
<img src="https://i.imgur.com/H1zRnro.png"/>
</p>


</br>
<h2>3. Create Organizational Units, Users, and Security Groups</h2>

- We then create 3 OUs, which are HR, IT, and Sales
- Then create 2 users in each respective OU
- Created 3 security groups, which are HR_Team, Sales_Team and IT_Team, so we assign permissions to a group rather than individually to users.
- Assigned members to those groups we created 

<p>
<img src="https://i.imgur.com/4qtpmTL.png"/>
</p>


</br>
<h2>4. Create File Shares and Permissions</h2>

- Created shared folders for each department, which are IT-TOOLs, SALES-REPORT, and HR_FILES
- Then, to make sure only respective departments have access to their files, we assigned NTFS permissions using groups.

<p>
<img src="https://i.imgur.com/tFyWlnw.png"/> <img src="https://i.imgur.com/zonmUSl.png"/>
</p>


</br>
<h2>5. Configuring Group Policies (GPO)</h2>

<h3>The first GPO we enforce is the password complexity policy. We want to make sure passwords created by users meet the complexity requirements for security purposes and link them </h3>

</br>
<p>
<img src="https://i.imgur.com/ARGikhi.png"/>
</p>

</br>
<br />
<h3>The second GPO we enforce is mapping network drives for our shared folders. We mapped all our folders to drives for easy access by our OUs </h3>

</br>
<p>
<img src="https://i.imgur.com/fg324fo.png"/> 
<img src="https://i.imgur.com/O9q6SXx.png"/>
</p>


</br>
<br />
<h3>The third GPO we enforce is making sure the control panel is disabled for our HR and Sales OU, as they do not need access to that </h3>

<p>
<img src="https://i.imgur.com/sYXfyI9.png"/> 
<img src="https://i.imgur.com/1NdLtRQ.png"/> 
</p>

<h2>Conclusion</h2>
<p>
This Active Directory home lab demonstrates the deployment and administration of a small enterprise domain environment. Through this project, I configured centralized identity management, implemented Group Policy security controls, and enforced role-based access using security groups and NTFS permissions.
</p>


