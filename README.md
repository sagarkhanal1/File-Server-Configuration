<h1>File Server with Advanced Permissions Project</h1>

<h2>Description</h2>
<!-- Documenting the setup of a file server with advanced permissions in a Windows Server environment -->
This project extends the SAGARDOMAIN setup by configuring a file server on Windows Server 2022 to host shared folders with NTFS and share permissions. It utilizes Active Directory groups to manage access for the 10 existing users, with detailed steps captured in screenshots.
<br />

<h2>Languages and Utilities Used</h2>
<!-- Listing the tools and utilities utilized in the project -->
<ul>
    <li><b>Server Manager</b></li>
    <li><b>File Explorer</b></li>
    <li><b>Active Directory Users and Computers</b></li>
</ul>

<h2>Environments Used</h2>
<!-- Specifying the operating systems used in the project -->
<ul>
    <li><b>Windows Server 2022</b> (Domain Controller/File Server)</li>
    <li><b>Windows 10</b> (21H2) (Client)</li>
</ul>

<h2>Project Walk-through:</h2>
<p style="font-size: 20px;">
<b>
<!-- Installing File Server Role -->
Installing File Server Role: <br/><br />
<img src="https://i.imgur.com/chTSax3.png" height="80%" width="80%" alt="File Server Role Install"/>
<br />
<span style="font-size: 16px;">The File Server role is installed via the "Add roles and features" wizard in Server Manager to enable file sharing capabilities.</span>
<br />
<br />
<!-- Creating Shared Folders -->
Creating Shared Folders: <br/><br />
<img src="https://i.imgur.com/AlfQcD2.png" height="80%" width="80%" alt="Shared Folders"/>
<br />
<span style="font-size: 16px;">Two folders, 'SharedDocs' and 'RestrictedDocs', are created on the server using File Explorer for different access levels.</span>
<br />
<br />
<!-- Creating AD Groups for Permissions -->
Creating AD Groups for Permissions: <br/><br />
<img src="https://i.imgur.com/ozKBPrA.png" height="80%" width="80%" alt="AD Groups"/>
<br />
<span style="font-size: 16px;">Two security groups, 'FileUsers' and 'FileAdmins', are created in Active Directory Users and Computers to manage folder access.</span>
<br />
<br />
<!-- Assigning Users to AD Groups -->
Assigning Users to AD Groups: <br/><br />
<img src="https://i.imgur.com/cpgCZee.png" height="80%" width="80%" alt="Assign Users"/>
<img src="https://i.imgur.com/TK5I290.png" height="80%" width="80%" alt="Assign Users"/>
<br />
<span style="font-size: 16px;">NTFS permissions are set, granting 'FileUsers' read access to 'SharedDocs' and 'FileAdmins' full control over both folders.</span>
<br />
<br />
<!-- Configuring Share Permissions -->
Configuring Share Permissions: <br/><br />
<img src="https://i.imgur.com/LxS7nuN.png" height="80%" width="80%" alt="NTFS Permissions"/>
<img src="https://i.imgur.com/2WDLqZm.png" height="80%" width="80%" alt="NTFS Permissions"/>
<br />
<span style="font-size: 16px;">Share permissions are configured, allowing 'FileUsers' read access and 'FileAdmins' change access to the shared folders.</span>
<br />
<br />
<!-- Sharing the Folders -->
Sharing the Folders: <br/><br />
<img src="https://i.imgur.com/J8E49Er.png" height="80%" width="80%" alt="Folder Sharing"/>
<img src="https://i.imgur.com/Ifeu68k.png" height="80%" width="80%" alt="Folder Sharing"/>
<br />
<span style="font-size: 16px;">The 'SharedDocs' and 'RestrictedDocs' folders are shared on the network with the configured permissions applied.</span>
<br />
<br />
<!-- Verifying Access from Windows 10 Client -->
Verifying Access from Windows 10 Client: <br/><br />
<img src="https://i.imgur.com/GrUPmB4.png" height="80%" width="80%" alt="Client Access"/>
<img src="https://i.imgur.com/Isz1E8g.png" height="80%" width="80%" alt="Client Access"/>
<br />
<span style="font-size: 16px;">A standard user logs into CLIENT1 and accesses 'SharedDocs' to confirm read-only access, while the admin tests full control.</span>
<br />
<br />
</b>
</p>
