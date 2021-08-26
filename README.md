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

Changes Path SDK:
C:\Android\Sdk

JDK Location:
C:\Program Files\Android\Android Studio\jre (Note: Gradle may be using JAVA_HOME when invoked from command line.

ANDROID STUDIO:

C:\Program Files\Android\Android Studio\bin
C:\Program Files\Android\Android Studio\jre\bin

System Variable:

ANDROID_HOME → SDK
C:\Android\Sdk

PATH:

%ANDROID_HOME%\platform-tools
%ANDROID_HOME%\tools
%ANDROID_HOME%\emulator
%ANDROID_HOME%\build-tools\31.0.0

System Variable:

JAVA_HOME
C:\Program Files\Java\jdk1.8.0_172

PATH:

%JAVA_HOME%\bin

```

## ANDROID LICENSES

```
gradle --stop


FAILURE: Build failed with an exception.

Checking the license for package Android SDK Platform 29 in C:\Android\Sdk\licenses
Warning: License for package Android SDK Platform 29 not accepted.

* What went wrong:
Could not determine the dependencies of task ':app:compileDebugJavaWithJavac'.
> Failed to install the following Android SDK packages as some licences have not been accepted.
     platforms;android-29 Android SDK Platform 29
  To build this project, accept the SDK license agreements and install the missing components using the Android Studio SDK Manager.
  Alternatively, to transfer the license agreements from one workstation to another, see http://d.android.com/r/studio-ui/export-licenses.html

  Using Android SDK: C:\Android\Sdk

SOLUTION:

C:\Android\Sdk\tools\bin

Open cmd and run next command:

sdkmanager --licenses

```

## GRADLE BUILD TOOL

```
https://gradle.org/
https://gradle.org/releases/

Download: binary-only

Step 1) Download Gradle files
https://gradle.org/

Step 2) Extract this file and place in C:
C:\Gradle\gradle-7.2

Step 3) Copy path then add in Environment Variables
C:\Gradle\gradle-7.2\bin

```

## SDK 31.0.0 is corrupted

```
What went wrong:
Could not determine the dependencies of task ':app:compileDebugJavaWithJavac'.
> Installed Build Tools revision 31.0.0 is corrupted. Remove and install again using the SDK Manager.

You may also need to do changes in SDK Manager under Tools, uninstall 31.0.0, and select Android R (API 30: version 11) to install 30.0.3

- Open Android Studio
- Manager Tools
- Uninstall SDK 31.0.0 and Platform 12
- Install SDK 30.0.3 and Platform 11

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

## Angular and Ionic (cordova)

```

npm install -g @angular/cli
npm install -g @angular/cli@11

npm install -g @ionic/cli
npm install -g @ionic/cli@5

npm uninstall -g ionic

npm i -g cordova
npm i -g cordova-res

```


