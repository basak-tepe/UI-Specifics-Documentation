# User Management Screen

##  Overview

This document outlines the UI specifications for the User Management screen, designed to allow administrators to manage user accounts within the system. The screen provides functionalities to view, filter, add, edit, and delete users.

## Requirements

1)  **User Table:** Display a list of users with ID,  User Name, Email, and Status (Enabled/Disabled).
2)  **Filter Options:** Provide filters to view users by ID, User Name, Email, and Status.
3)  **Add New User:** Include a button to add a new user, leading to a user form. 
4)  **User Form:** Include a form that takes credentials to create or edit a user record.
5)  **Save User:**  Include a button to create or edit a record from the filled user form.

## UI Layout and Components

### 1. **Header Section**
- **New User Button:**
  -  **Label:** "+ New User"
  - **Position:** Top left of the screen.
  - **Functionality:** Opens the "New User" form on the right side of the screen.
- **Hide Disabled User Checkbox:**
    - **Label:** "Hide Disabled User"
    - **Position:** Next to the "New User" button.
     - **Functionality:** When checked, the table filters out users with the "Enabled" status set to false.

### 2. **User List Table**
- **Columns:**
  -  **ID:** Displays the user's unique identifier.
  -  **User Name:** Displays the user's username.
  -  **Email:** Displays the user's email.
  -  **Enabled:** Displays the user's enabled status (true/false).
  
- **Filtering:**
  - Each column header contains a filter icon, allowing the user to filter the table data by the respective column.
  
- **Sorting:**
  - Users can sort the table by clicking on the column headers. An arrow icon indicates the current sort order (ascending/descending).
  
- **Table Behavior:**
  - Initially displays all users, sorted by the ID in ascending order.
  - Pagination may be required if the user list exceeds a certain number.
  

### 3. **New User Form**

- **Form Fields:**
  -  **Username:** Text input for the username.
  -  **Display Name:** Text input for the display name.
  -  **Phone:** Text input for the phone number.
  -  **Email:** Text input for the email adress.
  -  **User Roles:** Dropdown for selecting one or multiple user roles (Guest, Admin, SuperAdmin).
  -  **Enabled:** Checkbox to set the user status (checked for true, unchecked for false).

- **Save User Button:**
  -  **Label:** "Save User"
  - **Position:** Top right above of the form.
  - **Functionality:** Saves the user data and updates the user list table. If creating a new user, adds the new entry; if editing an existing user, updates the entry.


### 3. **Behavior and Interactions**
- **On Load:**
  - The user list table is populated with all existing users.
  - The "New User" form is hidden until "New User" button is clicked.
  
- **Adding a User:**
  - Clicking "+ New User" clears displays form fields and allows input for a new user.
  - Upon clicking "Save User," the new user is added to the table, and the form fields are cleared and hidden.

- **Editing a User:**
  - Selecting a user from the table populates the "New User" form with the user’s existing data.
  - Changes can be made, and clicking "Save User" updates the selected user’s information and hides the form.

- **Filtering Users:**
  - Filtering options in the table headers allow the user to narrow down the list based on ID, User Name, Email, or Enabled status.
  
- **Hide Disabled Users:**
  - When the "Hide Disabled User" checkbox is checked, users with the "Enabled" field set to false are hidden from the table.