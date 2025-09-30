# Streamlining-Ticket-Assignment-for-Efficient-Support-Operations
### Objective:
This project aims to design and implement an automated system on the ServiceNow platform that intelligently routes support tickets to the appropriate teams. This solution is intended to minimize resolution time, boost team efficiency, and enhance overall customer satisfaction.
### Skills Utilized:
- User and Group Management
- Role Management
- Table Configuration
- Access Control Lists (ACLs)
- Flow Designer (Automation)
### Modules Implemented:
- User Creation
- Role Assignment
- Group Creation
- Table Creation
- Assign Roles to Users and Groups
- Assign Role to Table
- ACL Creation
- Flows Creation and Activation
### 1. User & Group Management
As part of the project setup, I implemented User and Group Management to simulate real-world IT support operations. Each user was created to represent a specific role within the IT support hierarchy, ensuring proper role-based access and accountability. To streamline collaboration and task routing, I organized these users into dedicated groups aligned with their expertise.
- Specifically, I created two groups:
  - Certificate Group – responsible for handling certificate-related support requests.
  - Platform Group – responsible for managing platform-related issues.
- User Creation: Open ServiceNow > All > Search for Users > Select Users under System Security > Click New > Fill details and Submit.
- Group Creation:  Open ServiceNow > All > Search for Groups > Select Groups under System Security > Click New > Fill details and Submit.

This structure not only categorizes users effectively but also ensures that tickets are routed to the most suitable team, improving resolution efficiency.
#### Tasks Completed:
- Created individual users representing members of the support and platform teams.
- Established groups: Certificate Group and Platform Group.
- Assigned users to their respective groups based on domain expertise.
- Verified group memberships to ensure accurate ticket assignment and escalation paths.
### 2. Roles Creation & Assignment
To ensure secure and efficient access management within the ServiceNow instance, I implemented a structured Role-Based Access Control system. Roles were designed to define what actions users and groups could perform, such as viewing, editing, or managing specific data and components. By creating custom roles tailored to the IT support structure, I ensured that permissions aligned with the responsibilities of different teams and minimized the risk of unauthorized access.

These roles were strategically assigned not only to individual users but also to groups (e.g., Certificate and Platform) and the custom Operations Related Table. This helped enforce consistent access policies, streamline workflows, and maintain proper segregation of duties.
- Role Creation: Open ServiceNow > All > Search for Roles > Select Roles under System Security > Click New > Fill details and Submit.
#### Tasks Completed:
- Designed and created custom roles based on organizational access and security requirements.
- Assigned roles to appropriate entities for controlled access:
- Individual users – based on specific job functions.
- Groups (Certificate, Platform) – ensuring collective access aligned with team responsibilities.
- Custom tables (Operations Related Table) – to regulate who can create, view, and manage tickets.
- Validated role assignments to confirm that each user and group had the correct level of access without excessive permissions.
### 3. Table Creation
To manage and track Operations Related Tickets effectively, I designed and configured a custom table within the ServiceNow instance. This table was specifically created to store critical ticket-related information, including ticket ID, description, category, priority, and the group assigned for resolution.

By introducing a separate custom table, I ensured greater flexibility in tailoring the workflow, data structure, and automation rules to meet the unique requirements of the support process. Additionally, I implemented Access Control Lists (ACLs) to enforce role-based permissions, ensuring that only authorized users and groups could view or modify sensitive ticket data.
- Table Creation: Open ServiceNow > All > Search for Tables > Select Tables under System Definition > Click New > Fill details (columns) and Submit.
#### Tasks Completed:
- Created the custom table Operations_Related to store and manage Operations Support Tickets.
- Defined essential fields such as Request no., date, issue, priority, assigned group, and so on.
- Configured role-based access controls (ACLs) to regulate permissions for users, groups, and roles.
- Validated the table’s functionality to ensure smooth integration with the ticket routing workflow.
### 4. Assigning Roles to Users and Groups
After creating custom roles, I assigned them to both users and groups to ensure proper access control. Members of the Certificate Group received permissions for certificate-related tickets, while the Platform Group managed platform-related tickets. Roles were also applied to the Operations Related table to enforce secure ticket handling.  This multi-level assignment created a balanced approach—broad permissions could be applied to groups for efficiency, while specific users could still receive tailored access when needed.
- Role Assignment to Groups:
  - All > Groups under System Security > Certificates group > Edit Group members > Add Katherine Pierce > Save and assign Certification_role.
  - All > Groups > Platform group > Edit Group members > Add Manne Niranjan > Save and assign Platform_role.
- Role Assignment to Tables:
  - All > Operations Related > Application Access > u_operations_related read operation > Click Profile > Elevate role > Select Security Admin > Update > Insert Certification and Platform roles > Update.
#### Tasks Completed:
- Assigned roles to individual users to provide fine-grained access control.
- Assigned roles to groups (Certificate and Platform Groups) to streamline team-level permissions.
- Applied role-based access to the Operations Related table for secure ticket handling.
- Verified role assignments to ensure proper ticket visibility and prevent cross-access between unrelated groups.
### 5. Access Control Lists (ACLs)
To strengthen data security, I implemented Access Control Lists (ACLs) at both the table and field levels. These ACLs defined which actions—such as read, create, update, or delete—specific roles could perform on the Operations Related table. This ensured that only authorized users had access to ticket data. Additionally, field-level ACLs were configured to restrict sensitive information to administrative roles, protecting confidentiality and maintaining compliance with security best practices.
- ACLs Assignment: All > Search for ACL under System Security > Click New > Fill details and under Requires role, insert Admin Role.
#### Tasks Completed:
- Created ACLs to enforce table- and field-level security.
- Restricted read, write, update, and delete permissions to authorized roles.
- Applied field-level ACLs to limit access to sensitive data for non-admin users.
### 6. Flow Designer – Ticket Assignment Flows
Using Flow Designer, I created automated workflows to assign support tickets to the appropriate group based on ticket category. The first flow routes Certificate Issue tickets to the Certificate Group, while the second flow directs Platform Issue tickets to the Platform Group. These flows are triggered automatically whenever a new ticket is created, eliminating manual assignment, reducing errors, and ensuring faster response times.
- Flow 1: Assign Ticket to Certificate Group
  - Trigger: New Operations Ticket Created
  - Condition: Category = "Certificate Issue"
  - Action: Assign ticket to Certificate Group
- Flow 2: Assign Ticket to Platform Group
  - Trigger: New Operations Ticket Created
  - Condition: Category = "Platform Issue"
  - Action: Assign ticket to Platform Group

These flows ensure automatic ticket routing based on category, reducing manual intervention and improving response time.
### Conclusion
This project demonstrates the design and implementation of an Automated Ticket Assignment System using the ServiceNow platform. By configuring users, groups, roles, custom tables, ACLs, and automated flows, the system efficiently routes support tickets to the appropriate teams. Automation significantly reduced manual effort, improved response times, and enhanced overall operational efficiency.
The implementation of role-based access control ensured data security and maintained proper segregation of responsibilities. Through this project, I gained valuable hands-on experience in ServiceNow administration and observed how low-code platforms can effectively address real-world IT service management challenges.

---------------------------------------------------------------------------------
### Project Documentation link:
https://drive.google.com/file/d/19rMWwjLarye7Aj9oMS7erv_ANR11IuIo/view?usp=sharing

---------------------------------------------------------------------------------
### Here's the demo link of the project:
https://drive.google.com/file/d/1IH-JuUoJyY_Jf-sGXTOreTnMwWLPyb2e/view?usp=drive_link

---------------------------------------------------------------------------------
