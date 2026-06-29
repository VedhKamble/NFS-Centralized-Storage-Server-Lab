# NFS Centralized Storage Lab

## Project Overview

This project demonstrates the implementation of a centralized storage solution using Network File System (NFS) and AutoFS on Linux.

The setup includes multiple shared directories with different access controls, automatic mounting on client machines, and practical testing using two Linux systems.

---

## Lab Architecture

```text
              +----------------------+
              |     NFS Server       |
              |----------------------|
              | /exports/Public      |
              | /exports/Devs        |
              | /exports/Backup      |
              +----------------------+
                        |
                        | NFS
                        |
              +----------------------+
              |     NFS Client       |
              |----------------------|
              | AutoFS Configuration |
              | Group Permissions    |
              +----------------------+
```

## Technologies Used
Linux
NFS Server
AutoFS
firewalld
Linux Groups & Permissions

## Implemented Features
1) Public Share
    Location: /exports/Public
    Permissions:-
    Read: Everyone
    Write: Everyone

    Test Results:-
    File creation: Successful
    File modification: Successful
    File deletion: Successful
   
2) Development Share
    Location: /exports/Devs
    Permissions: Accessible only to members of the dev group
    Test Results:-
    Developers: Access granted
    Non-developers: Permission denied

3) Backup Share
    Location: /exports/Backup
    Permissions: Read-only
    Test Results:- 
    Reading files: Successful
    Creating files: Failed
    Modification attempts: Blocked

## AutoFS Integration

AutoFS was configured on the client machine to automate NFS mounting operations.
Features:-
a) Dynamic mounting on access
b) Automatic unmounting after inactivity
c) Reduced manual mount management

## Configuration Files
/etc/auto.master
/etc/auto.misc

Testing Summary
1) NFS Server Setup	
2) NFS Client Setup	
3) Public Share Access	
4) Developer Group Access	
5) Backup Read-Only Access	
6) AutoFS Configuration	
7) File Synchronization	
8) Client-Server Communication	

## Learning Outcomes
This project helped me practice:
1) NFS server deployment
2) Linux file sharing
3) Group-based access control
4) Read-only exports
5) AutoFS configuration
6) Network filesystem troubleshooting
7) Multi-machine Linux administration

Author
Vedh Kamble
Linux Server Administration Practice Project
