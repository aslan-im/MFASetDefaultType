# Remove-MFAPushMethod

The Remove-MFAPushMethod script is a PowerShell script that removes the PhoneAppNotification method from the MFA settings of an Azure AD user.
Prerequisites

This script requires the MSOnline PowerShell module to be installed on the machine running the script.

## Usage

Open PowerShell and navigate to the directory containing the Remove-PushMFAMethod.ps1 script.
Import the MSOnline module by running Import-Module MSOnline.
Execute the script by running:
```powershell
.\Remove-MFAPushMethod.ps1 -UserUpn "user@contoso.com"
```
replacing user@contoso.com with the user's UPN.

The script will check the MSOL connection and try to connect if it is not established. It will then retrieve the specified user and display their MFA settings before and after removing the PhoneAppNotification method.
Parameters

The script takes the following parameter:

    UserUpn: The user's UPN. This parameter is mandatory.

## Outputs

The script outputs the following:

- If the MSOL connection is not established, it will try to connect.
- If the specified user is found, it will display their MFA settings before and after removing the PhoneAppNotification method.
- If the PhoneAppNotification method is successfully removed, it will display a message saying so.
- If there is an error at any point, the script will display an error message.Remove-MFAPushMethod.ps1