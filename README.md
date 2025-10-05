# Pl-assignment-2--Tracy-Uwase


# Oracle Pluggable Database (PDB) Assignment  
**Student Name:** Tracy  
**Student ID:** 27105  
**Course:**  PL/SQL 

---

##  Executive Summary  
This assignment demonstrates hands-on skills in Oracle Multitenant Database Administration, focusing on **PDB creation, lifecycle management, and Enterprise Manager configuration**.  

---

##  Tasks Completed  

### Task 1: Create Permanent PDB  
- Created **`tr_pdb_27105`** with user **`tracy_plsqlauca_27105`** (`password`).  
- Granted roles: CONNECT, RESOURCE, DBA, UNLIMITED TABLESPACE.  
- Verified creation with `v$pdbs` and `dba_users`.  
- Configured **auto-open** on startup.  

 Result: Permanent PDB ready for coursework.  

**Screenshots:**  
- ![Screenshot 1: PDB Creation and Open Status](screenshorts/_01_pdb_open.png)  
- ![Screenshot 2: User Account Created](screenshorts/_02_user_created.png)  
- ![Screenshot 3: Privileges Granted](screenshorts/_03_privileges.png)  

---

### Task 2: Create & Delete Temporary PDB  
- Created **`tr_to_delete_pdb_27105`** with admin user.  
- Opened and verified with `v$pdbs`.  
- Closed and dropped with `INCLUDING DATAFILES`.  
- Confirmed only **`tr_pdb_27105`** remains.  

 Result: Demonstrated full PDB lifecycle management.  

**Screenshots:**  
- ![Screenshot 4: Temporary PDB Created](screenshorts/_04_temp_pdb.png)  
- ![Screenshot 5: Both PDBs Existing Together](screenshorts/_05_both_pdbs.png)  
- ![Screenshot 6: DROP Command Execution](screenshorts/_06_drop_command.png)  
- ![Screenshot 7: Verification - Temp PDB Deleted](screenshorts/_07_verified_deleted.png)  
- ![Screenshot 8: Only Permanent PDB Remains](screenshorts/_08_only_permanent.png)  

---

### Task 3: Configure Enterprise Manager Express (EM Express)  
- Set HTTPS port **5500**.  
- Logged in as SYSDBA, accessed **Dashboard**.  
- Verified:  
  - **Configuration → Pluggable Databases** → `tr_pdb_27105` OPEN.  
  - **Security → Users** → `tracy_plsqlauca_27105` visible.  
  - **PDB Details Page** accessible.  

 Result: OEM Express functional and monitoring enabled.  

**Screenshots:**  
- ![Screenshot 9: OEM Dashboard Homepage](screenshorts/_09_oem_dashboard.png)  
- ![Screenshot 10: PDB List in OPEN Status](screenshorts/_10_table%20view.png)  

---

##  Issues & Solutions  
- **Port Conflict:** Already configured → verified with query, reused port 5500.  
- **Wrong Container Context:** Initially in CDB instead of PDB → fixed using `ALTER SESSION SET CONTAINER`.  

---

##  Conclusion  
- **PDB Management mastered:** Creation, configuration, deletion.  
- **User Administration learned:** User setup, privileges, container context.  
- **OEM Express explored:** Dashboard, PDBs, users.  

The **permanent PDB `tr_pdb_27105`** is fully operational for PL/SQL coursework and future database administration exercises.  
