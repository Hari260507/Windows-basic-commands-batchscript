# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file
Save each script in a file with a .bat extension.
Ensure you have the necessary permissions to perform the operations.
Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "MyLab" on the desktop.
mkdir %userprofile%\Desktop\MyLab


<img width="202" alt="ex08 1" src="https://github.com/jayaseelan2006/Windows-basic-commands-batchscript/assets/151389443/98040f6d-4cd9-4c62-9df9-6893b2472e28">


## COMMAND AND OUTPUT

Change to the "MyLab" directory and create an empty text file named "MyFile.txt" inside it.
cd %userprofile%\Desktop\MyLab
type nul > MyFile.txt


<img width="169" alt="ex082" src="https://github.com/jayaseelan2006/Windows-basic-commands-batchscript/assets/151389443/80e67b0c-e23f-4c5a-9c41-2572ea30bd43">


## COMMAND AND OUTPUT

List the contents of the "MyLab" directory.
dir %userprofile%\Desktop\MyLab


<img width="205" alt="ex083" src="https://github.com/jayaseelan2006/Windows-basic-commands-batchscript/assets/151389443/af828746-aa6f-4d93-a024-64018daceece">



## COMMAND AND OUTPUT

Copy "MyFile.txt" to a new folder named "Backup" on the desktop.
mkdir %userprofile%\Desktop\Backup
copy MyFile.txt %userprofile%\Desktop\Backup


<img width="212" alt="ex084" src="https://github.com/jayaseelan2006/Windows-basic-commands-batchscript/assets/151389443/3c787a84-0dc7-40c0-95e2-795b6be5bd5f">



## COMMAND AND OUTPUT

Move the "MyLab" directory to the "Documents" folder.
move MyLab ..\Deocuments


<img width="176" alt="ex085" src="https://github.com/jayaseelan2006/Windows-basic-commands-batchscript/assets/151389443/4661e13c-7ec3-4d94-99b4-97db91e3c95e">




## COMMAND AND OUTPUT


## Exercise 2: Advanced Batch Scripting
Create a batch script named "BackupScript.bat" that creates a backup of files with the ".docx" extension from the "Documents" folder to a new folder named "DocBackup" on the desktop.
@echo off
mkdir %userprofile%\Desktop\DocBackup
copy %userprofile%\Documents\*.docx %userprofile%\Desktop\DocBackup
del %userprofile%\Documents\DocBackup\*.docx
echo Backup and deletion completed successfully!

Save the file and come back to command prompt.
Now execute as
BackupScript.bat

## OUTPUT

<img width="161" alt="ex086" src="https://github.com/jayaseelan2006/Windows-basic-commands-batchscript/assets/151389443/3a4bdf29-9979-4c2d-b503-77f58d83e8cd">

# RESULT:
The commands/batch files are executed successfully.

