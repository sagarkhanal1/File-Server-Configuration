# File Server Configuration Lab

A Windows Server lab demonstrating shared folder setup, NTFS permissions, share permissions, and Active Directory group-based access control.

## Project Summary

This project extends an Active Directory environment by configuring Windows Server 2022 as a file server. It uses security groups to control access to shared folders and validates the result from a Windows 10 domain-joined client.

The lab is designed to practise real IT support and systems administration tasks such as user access requests, permission troubleshooting, and secure file sharing.

## Skills Demonstrated

- Windows Server file server role configuration
- Shared folder creation
- NTFS permissions
- Share permissions
- Active Directory security groups
- Group-based access control
- Least privilege access concepts
- Client access testing
- Screenshot-based documentation

## Lab Environment

| Component | Technology |
|---|---|
| Server | Windows Server 2022 |
| Client | Windows 10 21H2 |
| Directory | Active Directory |
| Tools | Server Manager, File Explorer, Active Directory Users and Computers |

## Access Model

| Group | Access Purpose |
|---|---|
| FileUsers | Standard read access to shared documents |
| FileAdmins | Administrative access to shared and restricted folders |

## Project Walkthrough

### 1. Install File Server Role

The File Server role was installed through Server Manager to enable file sharing services.

<img src="https://i.imgur.com/chTSax3.png" height="80%" width="80%" alt="File Server Role Install"/>

### 2. Create Shared Folders

Two folders were created to represent different access levels: a shared documents folder and a restricted documents folder.

<img src="https://i.imgur.com/AlfQcD2.png" height="80%" width="80%" alt="Shared Folders"/>

### 3. Create Active Directory Groups

Security groups were created in Active Directory so permissions could be managed through group membership rather than individual user permissions.

<img src="https://i.imgur.com/ozKBPrA.png" height="80%" width="80%" alt="AD Groups"/>

### 4. Assign Users to Groups

Users were added to the correct Active Directory groups based on the access they required.

<img src="https://i.imgur.com/cpgCZee.png" height="80%" width="80%" alt="Assign Users"/>

<img src="https://i.imgur.com/TK5I290.png" height="80%" width="80%" alt="Assign Users"/>

### 5. Configure NTFS Permissions

NTFS permissions were configured to control local file system access on the server.

<img src="https://i.imgur.com/LxS7nuN.png" height="80%" width="80%" alt="NTFS Permissions"/>

<img src="https://i.imgur.com/2WDLqZm.png" height="80%" width="80%" alt="NTFS Permissions"/>

### 6. Configure Share Permissions

Share permissions were configured to control access over the network.

<img src="https://i.imgur.com/J8E49Er.png" height="80%" width="80%" alt="Folder Sharing"/>

<img src="https://i.imgur.com/Ifeu68k.png" height="80%" width="80%" alt="Folder Sharing"/>

### 7. Verify Access from Windows Client

A domain user logged into a Windows 10 client and tested access to confirm that permissions worked as expected.

<img src="https://i.imgur.com/GrUPmB4.png" height="80%" width="80%" alt="Client Access"/>

<img src="https://i.imgur.com/Isz1E8g.png" height="80%" width="80%" alt="Client Access"/>

## Key Takeaways

- Permissions should be assigned to groups, not individual users.
- NTFS permissions and share permissions work together.
- The most restrictive effective permission usually determines user access.
- Testing from a client machine is essential when validating access.
- File server administration is a practical skill for IT support and sysadmin roles.

## Future Improvements

- Add a diagram showing users, groups, and folders.
- Add a troubleshooting section for common access issues.
- Add PowerShell examples for creating folders and assigning permissions.
- Connect this scenario to the AI Help Desk project as a sample access request workflow.
