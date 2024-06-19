# **User Interface Specification Document**

## Overview
This document provides the specification for the user management screen. The screen allows administrators to view and create user accounts.

### Requirements
- **Display User List:** Show a table with all users, displaying their ID, User Name, Email, and Enabled status. 

- **Filter Disabled Users:** Option to hide or show disabled users.

- **Add New User:** Form to add new users with fields for Username, Display Name, Phone, Email, User Roles, and Enabled status.

- **Save User:** Button to save new user information.

### UI Compenents

- Header Section
  
   1. New User Button
   
      - Label: New User
      - Position: Positioned at the top left 
    
   2. Hide Disabled User Checkbox
   
      - Label: Hide Disabled User (this label should be bold)
      - Position: Positioned to the right of the New User button.

   3. Save User Button
   
      - Label: Save User
      - Position: Positioned at the top right


- Body Section
  
  1. User List Table
   
     - Label: N/A
     - Position: Below the header section, taking up the majority of the screen width.
     - Columns:
       - ID: (integer) Displays the unique identifier for each user.
       - Username: (text) Displays the username of the user.
       - Email: (text) Displays the email address of the user.  
       - Enabled: (text) Displays the status of the user (true/false).

  2. New User Form
   
     - Label: New User
     - Position: Right side of the user list table, taking up about half of the screen width. 
     - Fields:
       - Username
         - Label: Username: (this label should be bold) 
         - Description: The unique username for the new user.
         - Input Type: Text field
  
       - Display Name
         - Label: Display Name: (this label should be bold)
         - Description: The display name of the new user.
         - Input Type: Text field
  
       - Phone
         - Label: Phone:(this label should be bold)
         - Description: Text field
         - Input Type: The phone number of the new user.

       - Email
         - Label: Email: (this label should be bold)
         - Description: The email address of the new user.
         - Input Type: Text field

       - User Roles
         - Label: User Roles: (this label should be bold)
         - Description: The role assigned to the new user.
         - Input Type: Dropdown menu
         - Options: 
           - Guest
           - Admin
           - SuperAdmin
        
       - Enabled
         - Label: Enabled : (this label should be bold)
         - Description: Indicates whether the user account is active or inactive. If checked, the user account is active.
         - Input Type: Checkbox

### Initial State of The User Management Screen

- The Hide Disabled User checkbox is checked.
  
- The User List table is visible.

- The New User form is hidden.

### Behaviour of Components
  
- New User Button
  - When clicked 
    - The New User form becomes visible.

    - The User List table is pushed to the left side to place the form.

- Hide Disabled User Checkbox
  - If checked
    - The User List table doesn't show users whose Enabled status is false.
  - If unchecked 
    - The User List table shows all users.
  
- Save User Button
  - When clicked
    - The user data is saved.
  
    - The User List table is updated to include the new user.
  
    - The New User form is cleared and hidden.
    
- User List Table
    - Clicking on column headers should sort the list by that column.
    - If Hide Disabled User checkbox is checked, hide users where Enabled is false.
   
- New User Form
    - All fields are empty by default.
    - Enabled checkbox is unchecked by default.
    - User Roles dropdown menu says 'Select user roles...'.
  
