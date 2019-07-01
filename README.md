# Oracle-Database-Management-Pack
Open source free Oracle Database Management Pack for SCOM and Linux 


## About the Management Pack
This pack was created because there is no free alternative for monitoring Oracle Database.
I created a pack that is free for use and development.
feel free to modify and make changes to the project and please do update me on changes you want

This project is still under construction and for now, only the Discovery is working well and some monitors.
I will update the project with new monitors and collection rules in the near feature.

## Install instruction
You need to create an Oracle Database account with the next permissions in order to run the queries in the MP.
the permissions are:

```bash
grant connect to XXX;
grant select on DBA_DATA_FILES  to XXX;
grant select on dba_SCHEDULER_JOB_RUN_DETAILS   to XXX;
grant select on dba_users  to XXX;
grant select on dba_scheduler_jobs  to XXX;
grant select on V_$PARAMETER to XXX;
```

In the MP the account need to be attached to the "Oracle Linux Query Account" for it to run the discovery and monitors

## MP Structure is as follows:
Server
 Listener
  Instance
   TableSpace
    Schema
     Jobs
    Processes
    Alert Log
  
 ## If you have any questions or suggestions please contact [me](arlior@gmail.com)
