---
id: profile
title: Profile
sidebar_label: Profile
---


## Profile

This section explains how to create new profile in Oracle database. On profile, you can set limitations on database resource. The owner who is assigned a profile will have limited access to resourced defined by the profile. To create profile, owner’s ‘CREATE PROFILE’ privilege is required.

1. Connect to database.
2. On the main menu bar, go to **Create**>**Profile**.
3. Enter a name for the profile.
4. Select values for details on general tab.
![Create profile](https://s3.ap-northeast-2.amazonaws.com/sqlgate-manual-content/B0C1EAD903E20E250E337D2EFC1C8424.jpg)
The contents of general tab are given below:
- CPU/Session: CPU time limit on session.
- CPU/Call: CPU time limit on a call(Parser, Execute, Fetch, etc)
- Connect time: The total elapsed time limit for a session.
- Idle Time: The permitted periods of continuous active time during a session.
- Database service options are as followed
- Concurrent Sessions: The number of sessions running at the same time.
- Reads/Session: The number of data blocks session reads from memory and disk.
- Reads/Call: The number of data read from SQL Calls(Parse, Execute, Fetch etc.).
- Private SGA: The size of the private SGA space for a session.
- Composite Limit: The total resource cost for a session, expressed in service units

5. Set details for password tab.
![Set detailed options for profile password](https://s3.ap-northeast-2.amazonaws.com/sqlgate-manual-content/18D248A09C5838AEDFD2F42260862A11.jpg)
Options for password tab are as followed.
- Expired in: The number of days specified. The account will be expired after the given number of days.
- Lock (Days past expiration): The number of days an account will be locked if the password is not changed until the specified number of days.
- Number of passwords to keep: The number of passwords that can be kept.
- Number of days to keep: The number of days the passwords can be kept.
- Number of failed login attempts to lock after: If login attempts fail more than the given number, the account will be locked.
- Number of days to lock for: The number of days the account is locked for after failing to login.
- Complexity Function: It is a function that verifies password.
6. Click [View SQL] to check the autogenerated statements.
7. Click [OK] to check the result.

https://docs.oracle.com/cd/B19306_01/server.102/b14200/statements_6010.htm