---
author: joshbax-msft
title: BDE WLK Test - OS Volume Only
description: BDE WLK Test - OS Volume Only
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: dc006939-b473-45b8-b8ef-369121f4770c
---

# BDE WLK Test - OS Volume Only


This test verifies that Microsoft® Bitlocker does not cause data corruption on hard disks that are included in in a data array.

**Note**  
This test is only applicable to the hard disk that is configured as the boot drive.

 

## Test details


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Associated requirements</strong></p></td>
<td><p>Device.Storage.Controller.Boot.BitLocker Device.Storage.Hd.RaidArray.BitLocker</p>
<p>[See the device hardware requirements.](http://go.microsoft.com/fwlink/p/?linkid=254483)</p></td>
</tr>
<tr class="even">
<td><p><strong>Platforms</strong></p></td>
<td><p>Windows Server 2012 (x64) Windows Server 2012 R2</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expected run time</strong></p></td>
<td><p>~30 minutes</p></td>
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


Before you run the test, complete the test setup as described in the test requirements: [Hard Disk Drive Testing Prerequisites](hard-disk-drive-testing-prerequisites.md). This test requires 2 GB of unallocated disk space on the disk being tested.

## Troubleshooting


For troubleshooting information, see [Troubleshooting Device.Storage Testing](troubleshooting-devicestorage-testing.md).

## More information


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
<td><p>Bdewlktest.dll</p></td>
<td><p><em>&lt;[osbinroot]&gt;</em>\nttest\basetest\ngscb\</p></td>
</tr>
<tr class="even">
<td><p>Te.exe</p></td>
<td><p><em>&lt;[testbinroot]&gt;</em>\Testing\Runtimes\TAEF\x86\</p></td>
</tr>
</tbody>
</table>

 

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bp_hck\p_hck%5D:%20BDE%20WLK%20Test%20-%20OS%20Volume%20Only%20%20RELEASE:%20%284/27/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")



