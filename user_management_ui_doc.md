## User Interface Specification Document: User Management Screen

### Overview

The User Management Screen provides an interface for managing user accounts. The screen features a top toolbar and a user table, also including a user creation form for adding new users.

- **User Table:** 
  - **Purpose:** Displays a list of existing users.
  - **Columns:**
    - **ID:** Unique identifier for each user.
    - **Username:** The display name chosen for the user.
    - **Email:** The email address associated with the user.
    - **Enabled:** Indicates whether the user account is active or disabled, with values 'true' or 'false'.
  - **Sorting Functionality:** Users can click on column headers (ID, Username, Email, Enabled) to sort the table data in ascending or descending order.

- **Top Toolbar:** 
  - **New User Button:** When clicked, a user creation form slides in from the right side of the screen. A "Save User" button, initially disabled, appears on the right side of the top toolbar and becomes active once all required fields in the form are properly filled. Clicking "Save User" saves the new user and updates the user table.
  - **Hide Disabled Users Checkbox:** Allows users to filter the displayed user list to show only active (enabled) users.


### Initial State

Upon loading the page:
- The top toolbar is visible with the **New User** button and **Hide Disabled Users** checkbox.
- The user table is displayed below the toolbar, listing existing users with their details.
- The **User Creation Form** is hidden initially and slides in from the right side of the screen when the **New User** button is clicked.
- The **Save User** button appears on the right side of the top toolbar but is disabled until all required fields in the user creation form are properly filled.

### User Creation Form

#### Components

1. **Username Field**
   - **Type:** Text Input
   - **Label:** Username
   - **Validation:** Required, must be unique

2. **Display Name Field**
   - **Type:** Text Input
   - **Label:** Display Name
   - **Validation:** Required

3. **Phone Field**
   - **Type:** Text Input
   - **Label:** Phone
   - **Validation:** Optional, should follow a phone number format if provided

4. **Email Field**
   - **Type:** Email Input
   - **Label:** Email
   - **Validation:** Required, must be a valid email format

5. **User Roles Dropdown**
   - **Type:** Dropdown Menu
   - **Label:** User Roles
   - **Placeholder:** Select user roles...
   - **Options:**
     - Guest
     - Admin
     - SuperAdmin
   - **Validation:** Required

6. **Enabled Checkbox**
   - **Type:** Checkbox
   - **Label:** Enabled
   - **Default State:** Disabled (disabled by default)

7. **Save User Button**
   - **Type:** Button
   - **Label:** Save User
   - **Behavior:** On click, validate form fields and save user information. Initially disabled until all required fields are properly filled. If validation fails, display error messages.

### Behavior and Interaction

1. **Displaying the User Creation Form**
   - **Behavior:** Clicking the **New User** button slides in the user creation form from the right side of the screen. If the form is already visible, clicking the button will refresh or reset the form.

2. **Form Submission**
   - On clicking the **Save User** button, the form should be validated.
   - If validation is successful, the user data should be saved, and the user list table should be updated.
   - If validation fails, appropriate error messages should be displayed.

3. **Table Sorting**
   - Clicking on column headers should sort the table data in ascending or descending order.

4. **Hide/Show Disabled Users**
   - Checking or unchecking the **Hide Disabled Users** checkbox should dynamically update the user list table to show or hide users based on their 'Enabled' status.

### Visual Design

1. **Color Scheme**
   - **Primary Colors:**
     - **Background:** Predominantly white for most areas.
     - **Text on White Background:** Black text for readability.
     - **Text on Blue Background:** White text for contrast against the blue background.
   - **Buttons and Highlights:**
     - **Color:** Blue for buttons, column headers, and highlighted areas.
   - **Secondary Colors:**
     - **Backgrounds:** Grey is used to distinguish different sections such as the toolbar and form title.

2. **Button Design**
   - **Shape:** Rectangular.
   - **Color:** Blue for active buttons, less saturation for inactive buttons (e.g., Save User button is initially inactive).
   - **Size:** Large for primary actions (e.g., Save User button) and smaller for secondary actions if applicable.
   - **State:** Buttons change color based on their state (e.g., the Save User button).

3. **Item Hover Effect**
   - **Table Hover Effect:** When a table item is hovered over, it is highlighted with a light blue background, and the text becomes bold.
   - **Dropdown Hover Effect:** When a dropdown item is hovered over, it is highlighted with a light blue background, and the text becomes white and bold.
4. **Typography:**
   - **Font:** Standard web-safe font used (e.g., Arial or Roboto).

5. **Icons**
   - **New User Button Icon:** A plus sign icon to indicate adding a new user.
