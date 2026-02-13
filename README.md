# Update-DomainFederation.ps1

This PowerShell script is designed to update domain federation settings in Entra when federated to Omnissa Access. It provides options for safe testing and detailed output.

## Usage

### Basic Execution
To run the script normally with default settings, with and without parameters:
```powershell
./Update-DomainFederation.ps1
.\Update-DomainFederation.ps1 -TenantId "..." -Domain "customer.com" -MetadataUri "https://tenant.workspaceoneaccess.com/SAAS/API/1.0/GET/metadata/idp.xml" -BackupPath ".\backups\federation_backup.csv"
```

### WhatIf Mode (Safe Testing)
To test the script without making any actual changes:
```powershell
./Update-DomainFederation.ps1 -WhatIf
```

This mode shows you what would happen if you ran the script normally, allowing you to verify the changes before committing them.

### Verbose Mode (Detailed Output)
To run with detailed logging:
```powershell
./Update-DomainFederation.ps1 -Verbose
```

This provides step-by-step information about what the script is doing during execution.

### Combined Modes
You can combine both options for maximum visibility:
```powershell
./Update-DomainFederation.ps1 -WhatIf -Verbose
```

This will show you exactly what changes would be made and provide detailed logging throughout the process.

## Parameters
- `-WhatIf`: Simulates the operation without making changes (dry run)
- `-Verbose`: Provides detailed output about each step being executed

## Notes
- The script must be run with appropriate administrative privileges
- Ensure you have backed up your configuration before making changes
- Test with `-WhatIf` first to verify the intended behavior
