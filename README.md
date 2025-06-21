**Streamlining Ticket Assignment for Efficient Support Operations**
**Problem statement:**
The objective of this initiative is to implement an automated system for ticket routing at ABC Corporation
aimed at improving operational efficiency by accurately assigning support tickets to the appropriate teams.
This solution aims to reduce delays in issue resolution, enhance customer satisfaction, and optimize
resource utilization within the support department.

Activity 1: CREATE USERS
Open service now.
Click on All  >> search for users
Select Users under system security
Click on new
To fill data based on the given data

Activity 2: CREATE GROUPS
Open service now.
Click on All  >> search for groups
Select groups under system security
Click on new
To fill data based on the given data

Activity 3: CREATE ROLES
Open service now.
Click on All  >> search for roles
Select roles under system security
Click on new
To fill data based on the given data

Activity 4: CREATE TABLE
Open service now.
Click on All  >> search for tables
Select tables under system definition
Click on new
Fill the following details to create a new table
Label : Operations related
Check the boxes Create module & Create mobile module
Under new menu name : Operations related
Under table columns give the columns
After Creating table
Click on submit
Create choices for the issue filed by using form design
Choices are
unable to login to platform
404 error
regarding certificates
regarding user expired

Activity 5: Assign roles & users to certificate group
Open service now.
Click on All  >> search for tables
Select tables under system definition
Select the certificates group 
Under group members
Click on edit
Select Katherine Pierce and save
Click on roles
Select Certification_role and save

Activity 6:Assign roles & users to platform group
Open service now.
Click on All  >> search for tables
Select tables under system definition
Select the platform group 
Under group members
Click on edit
Select Manne Niranjan and save
Click on roles
Select Platform_role and save

Activity 7:Assign role to table
Open service now.
Click on All  >> search for tables
Select operations related table
Click on the Application Access
Click on u_operations_related read operation
Click on the profile on top right side
Click on elevate role
Click on security admin and click on update
Under Requires role
Double click on insert a new row
Give platform role
And add certificate role
Click on update
Click on u_operations_related write operation
Under Requires role
Double click on insert a new row
Give platform role
And add certificate role

Activity 8: Create ACL
Open service now.
Click on All  >> search for ACL
Select Access Control(ACL) under system security
Click on new
Fill the following details to create a new ACL
Scroll down under requires role
Double click on insert a new row
Give admin role
Click on submit
Similarly create 4 acl for the following fields

Activity 9: Create a Flow to Assign operations ticket to group
Open service now.
Click on All  >> search for Flow Designer 
Click on Flow Designer under Process Automation.
After opening Flow Designer Click on new and select Flow.
Under Flow properties Give Flow Name as “ Regarding Certificate”.
Application should be Global.
Select Run user as “ System user ” from that choice.
Click on Submit.

Click on Add a trigger 
Select the trigger in that Search for “create or update a record”  and select that.
Give the table name as “ Operations related ”.
Give the Condition as
Field : issue
Operator : is
Value : Regrading Certificates
After that click on Done.

Now under Actions.
Click on Add an action.
Select action in that search for “ Update Record ”.
In Record field drag the fields from the data navigation from left side
Table will be auto assigned after that 
Give the field as “ Assigned to group ”
Give value as “ Certificates ”
Click on Done.
Click on Save to save the Flow.
Click on Activate.

Activity 10: Create a Flow to Assign operations ticket to Platform group
Open service now.
Click on All  >> search for Flow Designer 
Click on Flow Designer under Process Automation.
After opening Flow Designer Click on new and select Flow.
Under Flow properties Give Flow Name as “ Regarding Platform ”.
Application should be Global.
Select Run user as “ System user ” from that choice.
Click on Submit.
Click on Add a trigger 
Select the trigger in that Search for “create or update a record”  and select that.
Give the table name as “ Operations related ”.
Give the Condition as
Field : issue
Operator : is
Value : Unable to login to platform
Click on New Criteria
Field : issue
Operator : is
Value : 404 Error
Click on New Criteria
Field : issue
Operator : is
Value : Regrading User expired 
After that click on Done.
Now under Actions.
Click on Add an action.
Select action in that search for “ Update Record ”.
In Record field drag the fields from the data navigation from left side
Table will be auto assigned after that 
Give the field as “ Assigned to group ”.
Give value as “ Platform ”.
Click on Done.
Click on Save to save the Flow.
Click on Activate.









