<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- OSTicketing system


<h2>Configuration Steps</h2>



<p>
<img width="837" height="555" alt="image" src="https://github.com/user-attachments/assets/521fdd85-8c8c-4095-b763-bafb4d3e72e4" />
<img width="872" height="847" alt="image" src="https://github.com/user-attachments/assets/ab4a2cc2-4ecd-4705-8f83-11667974ecca" />

</p>
<p>
  
Username and passwords
  
  <img width="607" height="721" alt="image" src="https://github.com/user-attachments/assets/85bcd60d-5f8f-4ba9-a390-673e1fd50417" />
  <img width="576" height="797" alt="image" src="https://github.com/user-attachments/assets/59ff5f5f-1d99-4498-99da-64d837022645" />


</p>
<br />

<p>
<img width="622" height="637" alt="image" src="https://github.com/user-attachments/assets/9e1a29bf-9fc0-40db-9341-39eeef092864" />
<img width="618" height="518" alt="image" src="https://github.com/user-attachments/assets/d20a2b74-26c8-4d2e-abad-4445eec743c3" />
<img width="622" height="838" alt="image" src="https://github.com/user-attachments/assets/453aa5d3-e1b7-475d-877e-1a51e23e244e" />
<img width="720" height="471" alt="image" src="https://github.com/user-attachments/assets/7f77d026-92f0-45d6-8301-27464bda57b5" />
<img width="830" height="327" alt="image" src="https://github.com/user-attachments/assets/bbecc035-e14d-4f92-bc9d-4eb4279d67ca" />
  
  tickets
  
<img width="873" height="566" alt="image" src="https://github.com/user-attachments/assets/0a181c40-aeab-4618-9445-7e3443d3359a" />
<img width="688" height="525" alt="image" src="https://github.com/user-attachments/assets/73ad57c4-82cf-48ea-9df7-c5560dde7e5b" />
<img width="902" height="476" alt="image" src="https://github.com/user-attachments/assets/83b1bbd6-aefb-45bc-a324-b37a5d0caaa1" />



</p>
<p>

	STEP 1 
	LOG IN
	
Admin/Analyst Login Page:
http://localhost/osTicket/scp/login.php 

End Users osTicket URL:
http://localhost/osTicket 

STEP 2

Acknowledge Agent Panel vs Admin Panel

Configure Roles (for grouping permissions)
Admin Panel -> Agents -> Roles
Supreme Admin

Configure Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)
Admin Panel -> Agents -> Departments
SysAdmins

Configure Teams
Admin Panel -> Agents -> Teams (Pull Agents from different Departments)
Online Banking

Allow anyone to create tickets
Admin Panel -> Settings -> User Settings (UNCHECK: unregistered users can create tickets)
Registration Required: Require registration and login to create tickets 

STEP 3

Configure Agents (workers)
Admin Panel -> Agents -> Add New
Jane (Dept: SysAdmins)
John (Dept: Support)

 STEP 4
 
Configure Users (customers)
Agent Panel -> Users -> Add New
Karen
Ken

STEP 5

Configure SLA
Admin Panel -> Manage -> SLA
Sev-A (Grace Period: 1 hour, Schedule: 24/7)
Sev-B (Grace Period: 4 hours, Schedule: 24/7)
Sev-C (Grace Period: 8 hours, Business Hours)

STEP 6

Configure Help Topics (For when users create a ticket)
Admin Panel -> Manage -> Help Topics
Business Critical Outage
Personal Computer Issues
Equipment Request
Password Reset
Other

-- Next

Admin/Analyst Login Page:
http://localhost/osTicket/scp/login.php 

End Users osTicket URL:
http://localhost/osTicket 

STEP 7

In this lab, we will be creating tickets as end users
Observing all the ticket properties and responding to them as help desk professionals

STEP 8

Change the SysAdmins Department to a Top Level Department
DELETE the Maintenance Department (not archive)

STEP 9

As an end-user, create the following ticket
entire mobile/online banking system is down

STEP 10

As a Help Desk Agent (john), observe the ticket’s properties
	Priority
	Department
	SLA
	Assigned To
STEP 11

Set Properties to the ticket
Sev-A (1 hour, 24/7)
Online Banking Department

Attempt to observe the ticket again as “john”. Can you view or change?

STEP 12

Work the ticket to completion as jane


STEP 13

As an end-user, create the following ticket
accounting department needs adobe upgrade, broken

STEP 14

As a Help Desk Agent (john), observe the ticket’s properties
	Priority
	Department
	SLA
	Assigned To
STEP 15

Set Properties to the ticket
Sev-B (4 hours, 24/7)
Support

Work the ticket to completion as john


STEP 16

As an end-user, create the following ticket
CFO’s laptop will no longer turn on

STEP 17

As a Help Desk Agent (john), observe the ticket’s properties
	Priority
	Department
	SLA
	Assigned To
STEP 18

Set Properties to the ticket
Sev-B (4 hours, 24/7)
Support

Work the ticket to completion as john

STEP 19

Set Properties to all the tickets; do SEV-A (SysAdmins last), observe ticket becomes inaccessible
Switch to admin panel and assign yourself View-access to Sys Admins
Switch to agent panel and observe the escalated ticket
Observe that you can no longer make changes to it

 STEP 20
 
Solve all of the tickets
Explain.
in most ticketing systems there is an email capability, so every time you update the ticket, the user gets a copy and they can respond

Explain ticket intake IRL:
Sometimes tickets get created via phone, chat app, email, web form, or maybe even you run into someone in your hall or they roll up on you at your desk.
A lot of the time people will randomize you and try to get you to fix stuff on the spot. It’s fine to fix things on the spot, but generally speaking, you want to create tickets for EVERYTHING you do. 

</p>
<br />
