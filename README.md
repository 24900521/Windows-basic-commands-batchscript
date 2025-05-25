# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

![Screenshot 2025-05-22 145810](https://github.com/user-attachments/assets/2afc1504-56d4-4260-874b-7fe50397ccf6)

## COMMAND AND OUTPUT

Remove the directory "my-folder"

![Screenshot 2025-05-22 145829](https://github.com/user-attachments/assets/ef69bb47-df73-4ca5-a660-ef850aa2d9c4)

## COMMAND AND OUTPUT

Create the file Rose.txt

![Screenshot 2025-05-22 145902](https://github.com/user-attachments/assets/e95ccbc0-1f69-416c-9e40-a596919bdf21)


## COMMAND AND OUTPUT

Create the file hello.txt using echo and redirection

![Screenshot 2025-05-22 145944](https://github.com/user-attachments/assets/b89e5403-858b-44b3-938c-adf4ef95b819)


## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt

![Screenshot 2025-05-22 150010](https://github.com/user-attachments/assets/2581d9fd-ad60-4580-9b8a-971349eff473)


## COMMAND AND OUTPUT

Remove the file hello1.txt

![Screenshot 2025-05-22 150026](https://github.com/user-attachments/assets/b9cec50b-f0c5-4e8c-8a88-ce1350b01d72)


## COMMAND AND OUTPUT

List out the file hello1.txt in the current directory

![Screenshot 2025-05-22 150124](https://github.com/user-attachments/assets/8bde9e5c-a533-4046-bd01-9459b44a2fd4)


## COMMAND AND OUTPUT

List out all the associated file extensions 

![Screenshot 2025-05-22 150203](https://github.com/user-attachments/assets/16ae10a9-042a-471d-a67d-c1a5b7a0fb6e)


## COMMAND AND OUTPUT

Compare the file hello.txt and rose.txt

![Screenshot 2025-05-22 150253](https://github.com/user-attachments/assets/fc46d1c9-d4ac-4439-b2a6-ee9542f4e12e)



## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
## Program
```
@echo off
set name=John
echo Hello, %name%
pause
```

## OUTPUT
![Screenshot 2025-05-23 135245](https://github.com/user-attachments/assets/ada03383-4173-4c6d-b4bf-9871820bbb1d)



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
## Program
```
@echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause
```


## OUTPUT
![Screenshot 2025-05-23 135700](https://github.com/user-attachments/assets/96ac615d-e786-46c0-afbf-db6ad47e1827)




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
## Program
```
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```

## OUTPUT
![Screenshot 2025-05-23 140200](https://github.com/user-attachments/assets/8e612c42-d80f-438a-9c4d-a6297a78a02a)




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.


Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
## Program
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
``` 

## OUTPUT
![Screenshot 2025-05-23 140414](https://github.com/user-attachments/assets/f076a39e-c53b-4d1b-9c9c-fb13e0432ffb)


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
## Program 
```
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit
```

## OUTPUT
![Screenshot 2025-05-23 140544](https://github.com/user-attachments/assets/3395d2f1-801b-440e-8663-697c2571f9e1)
![Screenshot 2025-05-23 140550](https://github.com/user-attachments/assets/f64652b2-dbb6-4f4c-848e-d04d4aa1a2f9)
![Screenshot 2025-05-23 140602](https://github.com/user-attachments/assets/b17f6cbe-2a30-4467-875f-949ac05a6a99)



# RESULT:
The commands/batch files are executed successfully.

