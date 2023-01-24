+++
author = "Nikolai Ahlhelm"
title = "Get all MSI Product Codes"
date = "2023-01-23"
description = "Get Product Codes of all applications installed via MSI"
categories = [
    "Powershell"
]
tags = [
    "Powershell",
    "Script"
]
image = ""
+++

The Product Codes are often required to make uninstallation of MSI applications easier. To get a ordered list of all product codes you just need to paste the following line in a powershell console.


{{< highlight powershell >}}
Write-Output(Get-WmiObject Win32_Product | Sort-Object Name | Format-Table IdentifyingNumber, Name -AutoSize)
{{< /highlight >}}