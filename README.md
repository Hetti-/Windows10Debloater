# Windows10Debloater
Script/Utility to debloat Windows 10

This script will remove the bloatware from Windows 10 and then delete specific registry keys that are not removed when using Rempve-AppXPackage/Remove-AppXProvisionedPackage.

It will also first ask you if you want to enable System Restore on your machine, then will create a restore checkpoint if you choose yes, ask if you want to continue to run the script, and if you choose 'Yes' you will then need to choose to either 'Debloat' or 'Revert'. Depending on your choice, either one will run specific code to either debloat your Windows 10 machine or to reinstall the bloatware and change your registry keys back to default. Finally, you will also have the choice to change some privacy settings at the end, such as disabling Cortana and stopping the Feedback Experience.

# Purpose

I have found many different solutions online to debloat Windows 10 and many either worked but caused issues in the long run, or they did so little that it wasn't enough of a "debloat" experience. I decided to create a script that will debloat Windows 10 the way that I envision it, with the option of even being able to revert changes.

This comes in hand when setting up new Windows 10 machines without needing to manually remove the bloatware found within Windows 10, along with some "fail safe" features via the Revert-Changes function, and even stops Windows from installing the bloatware in new user profiles.

# Silent and Interactive

There are now 2 versions of my Windows10Debloater - There is an interactive version, and a pure silent version. The silent version now utilizes the switch parameter: -Debloat. The silent version can be useful for deploying MDT Images or any other way you deploy Windows 10. This will work to remove the bloatware during the deployment process.

The interactive version is what it implies - a Windows10Debloater script with interactive prompts.

# How To Run

Download the Windows10Debloater.ps1 file. Next, copy the source code from Windows10Debloater.ps1 and throw it into PowerShell ISE.

Alternatively, download the Windows10DebloaterSilent.ps1 file, place it in any directory of your choice, load PowerShell ISE or PowerShell (64-Bit), change to the directory where you placed the Windows10DebloaterSilent.ps1 file, and add the switch parameter -Debloat: E.g., C:\Windows10DebloaterSilent.ps1 -Debloat

# Credit

Thank you to a60wattfish for some of the suggestions that I have placed into my scripts. 
