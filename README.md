# Install Modules

```powershell
Install-Module Microsoft.Graph -Scope CurrentUser
```

# Connect to Graph

```powershell
Connect-MgGraph -scopes "user.readwrite.all, group.readwrite.all"
```

# Set Variables

```powershell
$PWProfile = @{
    Password = "Pa55w.rd";
    ForceChangePasswordNextSignIn = $false
}
```

# Create New User

```powershell
New-MgUser `
    -DisplayName "Cody Godinez" `
    -GivenName "Cody" -Surname "Godinez" `
    -MailNickname "cgodinez" `
    -UsageLocation "US" `
    -UserPrincipalName "cgodinez@yourtenant.onmicrosoft.com" `
    -PasswordProfile $PWProfile -AccountEnabled `
    -Department "Sales" -JobTitle "Sales Rep"
```

# List Users

```powershell
Get-MgUser
