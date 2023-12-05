# Skriftuverkefni

### Skrifaðu forrit sem getur búið til notanda á Windows tölvu. Forritið á að spyrja um notendanafn, fullt nafn og lykilorð. Forritið notar svo þessar upplýsingar til að búa til notandann og setur hann í notendahópinn Users.

´´´ powershell 
$Username = Read-Host -Prompt "Enter the username"
$FullName = Read-Host -Prompt "Enter the full name"
$Password = Read-Host -Prompt "Enter the password" -AsSecureString

New-LocalUser -Name $Username -FullName $FullName -Password $Password -PasswordNeverExpires $true

Add-LocalGroupMember -Group "Users" -Member $Username

Write-Host "User $Username created and added to Users group."

# KEST2VW - Skilaverkefni 4 - (5%)

**Athugið að verkefnið er einstaklingsverkefni.** Ef tveir eða fleiri skila sömu lausn verður gefið 0 (núll) fyrir þær lausnir.

Skrifaðu forrit sem getur búið til notanda á Windows tölvu. Forritið á að spyrja um **notendanafn**, **fullt nafn** og **lykilorð**. Forritið notar svo þessar upplýsingar til að búa til notandann og setur hann í notendahópinn **Users**.

Dæmi um notkun:
```powershell
Sláðu inn notendanafn: geir
Sláðu inn fullt nafn: Geir Sigurðsson
Sláðu inn lykilorð: lykilorðið

Bý til notandann geir
```
Tryggið að notandinn sé búinn til, hann sé í notendahópnum Users og að hægt sé að skrá sig inn á Windows tölvuna sem hann.

Sýnið svo kennaranum kóðann virka og að hægt sé að skrá notandann inn. Skilið svo kóðanum á Innu.

Skipanir sem gott er að kynna sér:
```powershell
New-LocalUser
Get-LocalUser
Add-LocalGroupMember
```
