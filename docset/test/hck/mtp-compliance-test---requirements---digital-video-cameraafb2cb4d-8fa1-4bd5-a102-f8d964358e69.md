---
author: joshbax-msft
title: MTP Compliance Test - Requirements - Digital Video Camera
description: MTP Compliance Test - Requirements - Digital Video Camera
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 77c87c77-70c3-4ec2-a4a4-cce32e1842c1
---

# MTP Compliance Test - Requirements - Digital Video Camera


This device test validates compliance with the Picture Transfer Protocol (PTP) and Media Transfer Protocol (MTP).

This test makes sure that devices that use the MTP class driver comply with PTP and/or MTP implementation standards. This test is directed at digital video camera devices that use MTP. This test validates compliance with defined protocols based on requirements that are documented in the Windows Certification Program.

**Note**  
This test does not cover the following items:

-   Digital rights management (DRM) validation

-   Devices that use proprietary (third-party) drivers that work with the Windows Portable Device (WPD) driver stack

 

## Test details


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Associated requirements</strong></p></td>
<td><p>Device.Portable.DigitalVideoCamera.MTP</p>
<p>[See the device hardware requirements.](http://go.microsoft.com/fwlink/p/?linkid=254483)</p></td>
</tr>
<tr class="even">
<td><p><strong>Platforms</strong></p></td>
<td><p>Windows 7 (x64) Windows 7 (x86) Windows RT (ARM-based) Windows 8 (x64) Windows 8 (x86) Windows RT 8.1 Windows 8.1 x64 Windows 8.1 x86</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expected run time</strong></p></td>
<td><p>~5 minutes</p></td>
</tr>
<tr class="even">
<td><p><strong>Categories</strong></p></td>
<td><p>Certification Functional</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Automated</p></td>
</tr>
</tbody>
</table>

 

## Running the test


Before you run the test, complete the test setup as described in the test requirements: [Device.Portable Testing Prerequisites](deviceportable-testing-prerequisites.md).

This test copies test content to the device for testing. If the device is read-only, make sure the device has at least one file of each format type supported by the device.

## Troubleshooting


For troubleshooting information, see [Troubleshooting Device.Portable Testing](troubleshooting-deviceportable-testing.md).

## More Information


This test requires that a PTP or MTP-compatible device is installed using the MTP Class Driver. The test is fully automated with Pass/Fail results for each requirement.This test is divided into the following functional categories:

-   Device Capabilities tests

-   Operations tests

-   Object Property tests

Each functional category above contains child test cases, which test the subcomponents that fall under the corresponding category.

The test validates that the following operations are supported by the device:

-   OpenSession

-   CloseSession

-   GetDeviceInfo

-   GetStorageIDs

-   GetStorageInfo

-   GetNumObjects

-   GetObjectHandles

-   GetObjectInfo

-   GetObject

-   GetDevicePropDesc

-   GetDevicePropValue

All other supported operations, device properties, and object properties are considered optional and are therefore validated according to implementation details defined in the Picture Transfer Protocol (PTP) for Digital Still Photography Devices, Version 1.0 (PIMA15740) and Media Transfer Protocol (MTP), Revision 1.0. Please refer to the Certification Requirements for more information.

### Command syntax

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>te.exe /p:”BVT=TRUE” MtpTest.dll /select(@name='@CapabilitiesTests*') /p “DeviceProfile=MtpDigitalVideoCamera.xml”</strong></p></td>
<td><p>Runs the test.</p></td>
</tr>
</tbody>
</table>

 

**Note**  
For command-line help for this test binary, type **/h**.

 

### File list

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>File</th>
<th>Location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Mtptest.dll</p></td>
<td><p><em>&lt;testbinroot&gt;</em>\mtp\</p></td>
</tr>
<tr class="even">
<td><p>MtpDigitalVideoCamera.xml</p></td>
<td><p><em>&lt;testbinroot&gt;</em>\mtp\</p></td>
</tr>
</tbody>
</table>

 

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bp_hck\p_hck%5D:%20MTP%20Compliance%20Test%20-%20Requirements%20-%20Digital%20Video%20Camera%20%20RELEASE:%20%284/27/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")



