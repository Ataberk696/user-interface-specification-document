# User Management Screen Specification

## Overview
The User Management screen allows administrators to manage users in the system. This includes adding new users, editing existing users, and viewing a list of all users.

## Initial State
When the user management screen is first loaded, the following elements should be displayed:
1. A table listing existing users with columns for ID, User Name, Email, and Enabled status.
2. A "New User" button for adding a new user.
3. A "Hide Disabled User" checkbox to filter out disabled users from the table.
4. A form for adding or editing users with fields for Username, Display Name, Phone, Email, User Roles, and Enabled status.

## UI Components

### User List Table
- **Columns**: 
  - ID
  - User Name
  - Email
  - Enabled
- **Sorting**: 
  - The table columns should be sortable by clicking on the column headers.
- **Filtering**:
  - The "Hide Disabled User" checkbox should filter out users with `Enabled` status set to `false` when checked.

### New User Button
- **Function**: Opens the form to create a new user.
- **Behavior**: 
  - Clears the form fields.
  - Sets the form mode to "create".

### Hide Disabled User Checkbox
- **Function**: Toggles the visibility of disabled users in the user list table.
- **Behavior**:
  - When checked, users with `Enabled` status set to `false` are hidden.
  - When unchecked, all users are shown.

### User Form
- **Fields**:
  - Username (Text input)
  - Display Name (Text input)
  - Phone (Text input)
  - Email (Text input)
  - User Roles (Dropdown select with options: Guest, Admin, SuperAdmin)
  - Enabled (Checkbox)
- **Behavior**:
  - When adding a new user, the form is cleared and fields are enabled for input.
  - When editing an existing user, the form is populated with the user's information and fields are enabled for input.
  - The "Save User" button saves the user's information and updates the user list.

### Save User Button
- **Function**: Saves the information entered in the user form.
- **Behavior**:
  - Validates the form fields.
  - Sends the data to the backend to create or update the user.
  - Updates the user list table with the new or edited user information.

## Form Validation
- **Username**: Required
- **Email**: Required, must be a valid email format
- **User Roles**: Required

## Error Handling
- Display appropriate error messages if any form validation fails.
- Show a success message upon successful user creation or update.

