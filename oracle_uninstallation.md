## oracle Uninstallation - windows11

### 1. uninstall from control pannel

### 2. Delete Oracle Home Directory
  - C:\app\<YourUsername>\product\21.0.0\dbhome_1

### 3. Remove Oracle Registry Entries
  - Press Win + R, type regedit, and press Enter.
  - Navigate to the following keys and delete Oracle-related entries:
      - HKEY_LOCAL_MACHINE\SOFTWARE\ORACLE
      - HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services (search for Oracle services).
      - HKEY_CLASSES_ROOT\Installer\Products (search for Oracle products).

### 4. Remove Environment Variables
  - Under System Variables, look for and delete variables like
      - ORACLE_HOME
      - ORACLE_SID
      - PATH (remove Oracle-related paths)

### 5. Delete Oracle-Related Files
  - Delete any Oracle-related folders from:
      - C:\Program Files
      - C:\Program Files (x86)
      - %USERPROFILE% (check for .oracle or similar folders)
    
### 6. Remove from windows service
 - Open Run as services.msc
 - 
     <img width="660" alt="image" src="https://github.com/user-attachments/assets/a49cc372-366a-4d4e-8c9d-40f5aac54bd8" />

 - open cmd as administrator to delete below oracle service

   - sc delete OracleServiceORCL
   - sc delete OracleServiceXE
   - sc delete OracleJobSchedulerORCL
   - sc delete OracleJobSchedulerXE
   - sc delete OracleVssWriterORCL
   - sc delete OracleVssWriterXE
   - sc delete OracleOraDB21Home1MTSRecoveryService
   - sc delete OracleOraDB21Home1TNSListener
     
   <img width="374" alt="image" src="https://github.com/user-attachments/assets/829d16ff-ca47-4282-8d17-68cfdd47a53e" />

   
