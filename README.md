# Config Different Platforms

## Android Studio

* **How to Set Up Android Environment Variable Path on Windows 10**

```
Si es la primera vez:
Instalar Android Studio y al solicitar instalar SDK cambiar el Path

Caso contrario si es una reinstalación seguir los siguientes pasos:
Delete Folder Android:
C:\Users\Geo\AppData\Local\Android
Ctrl + R / %appData%

SDK Components Setup

Changes Path:
C:\Android\Sdk

JDK Location:
C:\Program Files\Android\Android Studio1\jre (Note: Gradle may be using JAVA_HOME when invoked from command line.

System Variable:

ANDROID_HOME
C:\Android\Sdk

PATH:

%ANDROID_HOME%\platform-tools
%ANDROID_HOME%\tools

System Variable:

JAVA_HOME
C:\Program Files\Java\jdk1.8.0_172

PATH:

%JAVA_HOME%\bin


```

## Visual Studio Code

```
Error PS1:

ionic --help

ionic : File C:\Users\name-user\AppData\Roaming\npm\ionic.ps1 cannot be loaded because running scripts is disabled on this system. For more 
information, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.
At line:1 char:1
+ ionic --help
+ ~~~~~
    + CategoryInfo          : SecurityError: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess


ng --version

ng : File C:\Users\name-user\AppData\Roaming\npm\ng.ps1 cannot be loaded because running scripts is disabled on this system. For more information, 
see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.
At line:1 char:1
+ ng --version

How To Fix Error PS1 Can Not Be Loaded Because Running Scripts Is Disabled On This System In Angular:


Solution
 
This error occurs when your system has disabled the running script and your system is can’t accept the ng commands.
This error occurs due to security reasons and won't let the script be executed on your system without your approval.
Then you have to open the PowerShell with administrative rights.

To solve this problem, you need to follow a few steps:



Step 1

First, you have to need to open the command prompt (PowerShell Run as administrator) and run this command.

~$ set-ExecutionPolicy RemoteSigned -Scope CurrentUser

When you run this command, you can see that your system has set all policies for the current user as remotely.
It will take few seconds to complete this process.

Step 2

Now you have to run the second command on your system. This command is:

Get-ExecutionPolicy

When you have run this command your system has a show “RemoteSigned”. If you have received this message,
then your problem will be solved. Now you have to go to the next step to view the list of policy which policy
has been updated by the last commands.

To shown this messge:

~$ RemoteSigned

Step 3

To view their policy, you need to run this command in your command prompt:

~$ Get-ExecutionPolicy -list

When you run this command, a few policies are shown on your monitor screen. These policies are:

Scope ExecutionPolicy
----- ---------------
MachinePolicy Undefined
UserPolicy Undefined
Process Undefined
CurrentUser RemoteSigned
LocalMachine Undefined
CurrentUser RemoteSigned
LocalMachine Undefined


Now you can see your system execution policy list. You have successfully solved your problem.
Now you need to go to the command prompt and check that your problem is solved.

```



