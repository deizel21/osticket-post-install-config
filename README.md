<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configuring Roles, Groups and Teams
- Configuring Agens/Admins , Users and Permissions 
- Setting Service Level Agreements(SLA's)
- Configuring a Help Topic

<h2>Configuration Steps</h2>

• Login in to the Admin/Analyst Login Page: ( http://localhost/osTicket/scp/login.php )

End Users osTicket URL:
http://localhost/osTicket 

Acknowledge Agent Panel (Help Desk support) vs Admin Panel (System Admin)

Configure Roles (Info for grouping permissions)
•	Select Admin Panel in the top right -> Then select Agents -> Then Roles > Then Add New Role > type Supreme Admin >  Permissions and select all permissions   for tickets, task and Knowledgebase tabs > Add role

Configure Departments (Info for Ticket Visibility, Help Desk vs SysAdmins, vs Networking)
Admin Panel -> Agents -> Top level Departments > then type SysAdmins in name bar > then scroll down and press Create Dept

Configure Teams 
Admin Panel -> Agents -> Teams (Pull Agents from different Departments) > Click the Add New Teams button > Type Online Banking in Name section > Select Create team button

![image](https://github.com/user-attachments/assets/38291f7f-1e0e-48cd-ab3e-e52ea1a1c081)
![image](https://github.com/user-attachments/assets/4e0e2fb8-2817-4f80-a8cf-5dd776937e73)
![image](https://github.com/user-attachments/assets/2b439c48-7c47-4a9f-acf1-d9b1dfd04722)
![image](https://github.com/user-attachments/assets/64c5d546-9410-4375-b6f0-5d7344c03410)
![image](https://github.com/user-attachments/assets/782d3d8b-4b24-43f4-89d5-900cc80d58e6)

•	Allow anyone to create tickets for the purpose of this lab ONLY!
Admin Panel -> Settings -> User Settings UNCHECK:Registration Required: Require registration and login to create tickets 

 	 (The UNCHECK : allows unregistered users to create tickets for the purpose of this lab)

Configure Agents (workers)
Admin Panel -> Agents -> Add New
	Jane Doe (Dept: SysAdmins) , email :Jane@lognpacific.com , set password to Password 1, uncheck Require Password on next login, Access: Primary Department (Select SysAdmins and Supreme Admin) , Teams: Select Online banking and then create. 
	John (Dept: Support) , email :John@lognpacific.com , set password to Password 1, uncheck Require Password on next login,  Access: Primary Department (Select SysAdmins and Supreme Admin) , Teams: Select Online banking and then create.

•	Configure Users (customers)
Agent Panel -> Users -> Add New 
•	Add email Karen@lognpacific.com, username karen > add user
•	Add email Ken


![image](https://github.com/user-attachments/assets/f105f9ea-113b-4cb3-a353-91067abfe7e2)
![image](https://github.com/user-attachments/assets/7a9f0e1f-9acc-49ab-af86-7c7541712179)
![image](https://github.com/user-attachments/assets/5164232e-d911-44c9-8f9e-f5c560a2d687)
![image](https://github.com/user-attachments/assets/85a7ae84-0e3c-418a-b78c-e7b7a2333d58)

Make sure everything is filled out correctly!

•	Configuring a SLA (Basically means how much time you have to do a task/ticket)
Click the Admin Panel -> Manage -> SLA > then Add New SLA Plan
•	Sev-A (Grace Period: 1 hour, Schedule: 24/7)
•	Sev-B (Grace Period: 4 hours, Schedule: 24/7)
•	Sev-C (Grace Period: 8 hours, Monday-Friday Normal Business Hours)
Sev-A = High Priority  Sev – B  = Medium level Priority Sev C = Low Priority

![image](https://github.com/user-attachments/assets/9ddf186f-a6c4-4bee-8515-292050dfb714)

•	Configure Help Topics (For when users create a ticket)
  Admin Panel -> Manage -> Help Topics > Add New Help Topic
	Business Critical Outage > Select Parent Topic dropdown and choose Report a problem

•	Personal Computer Issues> Select Parent Topic dropdown and choose Report a problem
  Equipment Request> Select Parent Topic dropdown and choose General Inquiry 

•	 Password Reset> Select Parent Topic dropdown and choose Report a problem
  Other> Select Parent Topic dropdown and choose General Inquiry

  ![image](https://github.com/user-attachments/assets/24cceea4-6ca3-4b9f-bfc6-9fa0fa770931)

Congrats! You should now have completed the post installation process for osTicket.
