# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript
# NAME : SUMAIYA S
# REGISTER NO : 212225040437
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

## COMMAND AND OUTPUT

Remove the directory "my-folder"

## COMMAND AND OUTPUT

<img width="780" height="136" alt="image" src="https://github.com/user-attachments/assets/5b2e6409-718b-474f-8656-b45912e63d5b" />

Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="962" height="367" alt="image" src="https://github.com/user-attachments/assets/de1086a6-2e3c-4605-88e4-a15a448baee9" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

<img width="890" height="120" alt="image" src="https://github.com/user-attachments/assets/91a791cd-5330-4601-9379-030209db0846" />


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

<img width="917" height="146" alt="image" src="https://github.com/user-attachments/assets/f2459e7a-00e5-4065-b6c3-6bb1d8d6fa5b" />


Remove the file hello1.txt

## COMMAND AND OUTPUT

<img width="891" height="236" alt="image" src="https://github.com/user-attachments/assets/fd09412f-b6ff-4636-9825-6c0f615089a4" />


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT:

<img width="579" height="181" alt="image" src="https://github.com/user-attachments/assets/d47a9f3d-cba2-4dc5-afde-22870efb5948" />


List out all the associated file extensions 

## COMMAND AND OUTPUT

<img width="856" height="912" alt="image" src="https://github.com/user-attachments/assets/00db55a1-4dd9-427c-a61a-0c492c3f5b3b" />



Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT:

<img width="726" height="222" alt="image" src="https://github.com/user-attachments/assets/64424f3a-6e5e-4ed8-b1c2-a66d0abbcebe" />


## Exercise 2: Advanced Batch Scripting
# Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```
@echo off
set name=John
echo Hello, %name%!
pause
```

## OUTPUT

<img width="623" height="95" alt="image" src="https://github.com/user-attachments/assets/077a0382-ba17-4b4c-8692-03f79441eb3f" />


# Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
1. Prompt the user to enter a number.
2. Calculate the remainder when the number is divided by 2.
3. Display whether the number is odd or not.
4. Ask the user if they want to check another number.
5. Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
6. Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
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

```



## OUTPUT

<img width="861" height="241" alt="image" src="https://github.com/user-attachments/assets/03bc81c8-5f7c-45c9-8248-e2947acabc5b" />


# Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

```


## OUTPUT

<img width="748" height="184" alt="image" src="https://github.com/user-attachments/assets/9bcbc078-a8a8-4973-841c-66fb5b444b75" />



# Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
1. Use the IF EXIST conditional statement.
2. Make sure the script works for files located in the same directory as the batch file.
3. Use pause to keep the command window open after displaying the message.
4. Expected Output (if the file exists):

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

<img width="905" height="228" alt="image" src="https://github.com/user-attachments/assets/9c2c7a89-ca85-4072-9ac8-6736e201a2f2" />



# Write a batch script that displays a simple menu with three options:
1. Say Hello – Displays the message Hello, World!
2. Create a File – Creates a file named newfile.txt with the content This is a new file
3. Exit – Exits the script with a goodbye message
4. The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause

```

## OUTPUT

<img width="707" height="423" alt="image" src="https://github.com/user-attachments/assets/26889464-a837-4cb4-9d6f-b9d1d39e9482" />


# RESULT:
The commands/batch files are executed successfully.

