---
author: joshbax-msft
title: NVMe Interrupt Modes Test (LOGO)
description: NVMe Interrupt Modes Test (LOGO)
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 39dadef0-4b4b-49e3-86a0-31430e58dd02
---

# NVMe Interrupt Modes Test (LOGO)


This test verifies the device’s capability of operating in different interrupt mode by doing I/O. The following are the various interrupt modes exercised:

-   Random number of interrupts (Power of 2) in MSI-X/MSI mode

-   1 MSI-X/MSI mode

-   Line Based interrupt mode

## Test details


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Associated requirements</strong></p></td>
<td><p>Device.Storage.ControllerDrive.NVMe.BasicFunction</p>
<p>[See the device hardware requirements.](http://go.microsoft.com/fwlink/p/?linkid=254483)</p></td>
</tr>
<tr class="even">
<td><p><strong>Platforms</strong></p></td>
<td><p>Windows 8.1 x64 Windows 8.1 x86 Windows Server 2012 R2</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expected run time</strong></p></td>
<td><p>~60 minutes</p></td>
</tr>
<tr class="even">
<td><p><strong>Categories</strong></p></td>
<td><p>Certification Reliability</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Automated</p></td>
</tr>
</tbody>
</table>

 

## Running the test


Before you run the test, complete the test setup as described in the test requirements: [Hard Disk Drive Testing Prerequisites](hard-disk-drive-testing-prerequisites.md).

## Troubleshooting


For troubleshooting information, see [Troubleshooting Device.Storage Testing](troubleshooting-devicestorage-testing.md).

If the test fails to find the drive letter of the device, try to restart the machine with device attached, format and mount NTFS volume and assign drive letter, reboot machine to confirm drive letter and drive number of device are recognizable in diskmgmt.msc and then schedule the test.

 

 





