# Skriftuverkefni

### Skrifaðu forrit sem getur búið til notanda á Windows tölvu. Forritið á að spyrja um notendanafn, fullt nafn og lykilorð. Forritið notar svo þessar upplýsingar til að búa til notandann og setur hann í notendahópinn Users.

``` powershell 
$Username = Read-Host -Prompt "Enter the username"
$FullName = Read-Host -Prompt "Enter the full name"
$Password = Read-Host -Prompt "Enter the password" -AsSecureString

New-LocalUser -Name $Username -FullName $FullName -Password $Password -PasswordNeverExpires $true

Add-LocalGroupMember -Group "Users" -Member $Username

Write-Host "User $Username created and added to Users group."
```
