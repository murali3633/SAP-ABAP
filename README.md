# Faculty and Student Management System

This project is an SAP ABAP Module Pool application designed to manage Faculty and Student details. It provides a user-friendly interface for registration, login, and data management based on user roles.

## Project Overview

The application streamlines the process of maintaining records for an educational institution. It classifies users into two categories:
- **Faculty**: Can view and manage both faculty and student details.
- **Student**: Can view student details and manage their own profile.

## Features

- **User Authentication**: Secure Login and Registration system.
- **Role-Based Access Control**:
  - **Faculty**: Access to full database views (Faculty list, Student list).
  - **Student**: Restricted access (Student list).
- **Dashboard**: Centralized hub for navigation.
- **Data Management**: Forms to add/edit Faculty and Student information.

## Technical Details

### Architecture
- **Type**: SAP ABAP Module Pool (Online Transaction Processing).
- **Main Program**: `ZCSE1` (refer to `Codes/MAIN.txt`).

### Components

#### Custom Database Tables
- **`ZLOGIN`**: User credentials and role mapping.
- **`ZFACULTY`**: Master data for Faculty.
- **`ZSTU`**: Master data for Students.

#### Screens (Dynpros)
- **140**: Login Screen
- **141**: Registration Screen
- **142**: Faculty Dashboard
- **143**: Intermediate/Redirect Screen
- **144**: Faculty List Display
- **145**: Student List Display
- **146**: Faculty Data Entry/Edit
- **147**: Student Data Entry/Edit

## Installation

To import this project into your SAP environment:

1.  **Create Custom Tables**: Create `ZLOGIN`, `ZFACULTY`, and `ZSTU` in SE11 with the fields described in the code analysis.
2.  **Create Main Program**: Create a Module Pool program named `ZCSE1` in SE80.
3.  **Import Code**:
    - Copy the content of `Codes/MAIN.txt` into the main program.
    - Create the Include programs (`ZCSE_MAIN_TOP`, `ZCSE1_STATUSMODULE`, etc.) and paste the corresponding code from the `Codes/` directory.
4.  **Create Screens**: Create screens 140 through 147 in Screen Painter (SE51) and define the Element Lists and Flow Logic as per the `SCREEN xxx.txt` files.
5.  **Activate**: Activate all objects.

## Screenshots

### Login Screen
![Login Screen](Output/login%20screen.png)

### New Account Registration
![New Account](Output/new%20account.png)

### Faculty Dashboard
![Faculty Info](Output/faculty.png)

