# Create an Azure Virtual Network with PowerShell

Run the following commands in PowerShell to create an Azure Virtual Network

```PowerShell
# Replace the following required Azure Virtual Network variables
$vNet = @{
    Name = 'your-vnet-name'
    ResourceGroupName = 'your-rg-name'
    Location = 'EastUS2'
    AddressPrefix = '10.0.0.0/16'
}

# Create the VNet
$virtualNetwork = New-AzVirtualNetwork @vnet
```

## Notes

Display all available Azure locations

```PowerShell
Get-AzLocation | Format-Table -Property Location, DisplayName
```

## Troubleshooting

## Alternatives

## Additional Resources

- [MS | Docs | New-AzVirtualNetwork][1]
- [MS | Docs | Get-AzLocations][2]

<!-- Reference Links -->

[1]: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork?view=azps-5.7.0
[2]: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation?view=azps-5.7.0
