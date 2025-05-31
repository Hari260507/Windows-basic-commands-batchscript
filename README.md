Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

AIM:
To execute Windows basic commands and batch scripting

DESIGN STEPS:
Step 1:
Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware

Step 2:
Write the Windows commands / batch file Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.

Step 3:
Execute the necessary commands/batch file for the desired output.

WINDOWS COMMANDS:
Exercise 1: Basic Directory and File Operations
Create a directory named "MyLab" on the desktop.

mkdir %userprofile%\Desktop\MyLab
alt text

mkdir my-folder

![image](https://github.com/user-attachments/assets/3daad5c4-f131-4d0a-91e9-445c3758938e)

rmdir my-folder

![image](https://github.com/user-attachments/assets/3fe9936b-feb0-4737-b728-07375d4aae22)


COMMAND AND OUTPUT
Change to the "MyLab" directory and create an empty text file named "MyFile.txt" inside it.

mkdir %userprofile%\Desktop\MyLab




COPY CON Rose.txt
A clock in a office can never get stolen
Too many employees watch it all the time

![image](https://github.com/user-attachments/assets/9e822880-68a4-4823-9e88-4196ff85fc94)




dir Rose.txt

![image](https://github.com/user-attachments/assets/db6d1a70-fe18-41a9-872c-3603da8c906f)


echo hello world > hello.txt
![image](https://github.com/user-attachments/assets/0de904d3-525b-417b-ac8e-76cbbc9d8519)



type hello.txt
copy hello.txt hello1.txt
del hello1.txt

alt text

COMMAND AND OUTPUT
List the contents of the "MyLab" directory.

cd %userprofile%\Desktop\MyLab
![image](https://github.com/user-attachments/assets/f86b66b3-35bf-4101-a678-989101738a57)


type nul > MyFile.txt

![image](https://github.com/user-attachments/assets/428b71fc-b989-4c1c-9a56-96824097f5b9)


assoc | more
![image](https://github.com/user-attachments/assets/4b520820-7889-4b35-83be-4f384a0f3f4f)



fc hello.txt Rose.txt

![image](https://github.com/user-attachments/assets/ddb389a5-034a-45c6-bf8a-adafa392863c)


COMMAND AND OUTPUT
Copy "MyFile.txt" to a new folder named "Backup" on the desktop.

dir %userprofile%\Desktop\MyLab
![image](https://github.com/user-attachments/assets/2fe424d2-311c-466b-a988-9a192ea7274c)


COMMAND AND OUTPUT
Move the "MyLab" directory to the "Documents" folder.

mkdir %userprofile%\Desktop\Backup
![image](https://github.com/user-attachments/assets/f105d3cb-e104-49aa-a20f-ca2d23349dae)

copy MyFile.txt %userprofile%\Desktop\Backup
![image](https://github.com/user-attachments/assets/1ef88ce5-5598-4be4-88c3-27e627a51ec3)


COMMAND AND OUTPUT
mkdir %userprofile%\Desktop\Documents
![image](https://github.com/user-attachments/assets/0e0b0ebe-7e93-44e2-8540-1f00b744bc56)


Exercise 2: Advanced Batch Scripting
Create a batch script named "BackupScript.bat" that creates a backup of files with the ".docx" extension from the "Documents" folder to a new folder named "DocBackup" on the desktop.

OUTPUT
1.BAT:
@echo off
set name=John
echo Hello, %name%!
pause


![image](https://github.com/user-attachments/assets/e93aed89-721f-4aca-a15d-1bec9859a621)


2.BAT
@echo off
:main
set /p number=Enter a number: 
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause

![image](https://github.com/user-attachments/assets/662ffd2b-e92d-411e-a48f-a8e985f3c2dc)


3.BAT
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause


![image](https://github.com/user-attachments/assets/041c3918-4217-45d0-afaa-55772d65bb27)


4.BAT
@echo off
echo Reading lines from sample.txt...
for /f "tokens=*" %%i in (sample.txt) do (
    echo Fruit: %%i
)
pause

![image](https://github.com/user-attachments/assets/cf95bd2e-1964-4bdb-b3ed-19daf485d7fc)


5.BAT
@echo off
echo Displaying Even or Odd for numbers 1 to 10
for /l %%i in (1,1,10) do (
    set /a rem=%%i %% 2
    if %%i %% 2 == 0 (
        echo %%i is Even
    ) else (
        echo %%i is Odd
    )
)
pause

![image](https://github.com/user-attachments/assets/6200715c-dce8-4491-8fbf-8825124dc191)


RESULT:
The commands/batch files are executed successfully
