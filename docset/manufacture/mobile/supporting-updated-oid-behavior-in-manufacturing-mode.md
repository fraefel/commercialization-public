---
Description: Supporting updated OID behavior in manufacturing mode
MS-HAID: 'p\_phManuRetail.supporting\_updated\_oid\_behavior\_in\_manufacturing\_mode'
MSHAttr: 'PreferredLib:/library/windows/hardware'
title: Supporting updated OID behavior in manufacturing mode
---

# Supporting updated OID behavior in manufacturing mode


When running in manufacturing mode, Wi-Fi miniport drivers must add support for the following updated OIDs.

## <span id="OID_DOT11_OPERATION_MODE_CAPABILITY"></span><span id="oid_dot11_operation_mode_capability"></span>OID\_DOT11\_OPERATION\_MODE\_CAPABILITY


The **OID\_DOT11\_OPERATION\_MODE\_CAPABILITY** command is called in query mode to return the list of operation modes supported by the driver. This command functions as previously documented, but drivers are now required to support a new operation mode, **DOT11\_OPERATION\_MODE\_MANUFACTURING**, which is the context in which manufacturing operations are performed. For complete documentation of this OID, see [OID\_DOT11\_OPERATION\_MODE\_CAPABILITY](http://msdn.microsoft.com/library/ff569396.aspx) on MSDN.

``` syntax
#define DOT11_OPERATION_MODE_UNKNOWN            0x00000000
#define DOT11_OPERATION_MODE_STATION            0x00000001
#define DOT11_OPERATION_MODE_AP                 0x00000002
#define DOT11_OPERATION_MODE_EXTENSIBLE_STATION 0x00000004
#define DOT11_OPERATION_MODE_EXTENSIBLE_AP      0x00000008
#define DOT11_OPERATION_MODE_WFD_DEVICE         0x00000010
#define DOT11_OPERATION_MODE_WFD_GROUP_OWNER    0x00000020
#define DOT11_OPERATION_MODE_WFD_CLIENT         0x00000040
#define DOT11_OPERATION_MODE_MANUFACTURING      0x40000000
#define DOT11_OPERATION_MODE_NETWORK_MONITOR    0x80000000

typedef struct _DOT11_OPERATION_MODE_CAPABILITY {
    ULONG uReserved;
    ULONG uMajorVersion;
    ULONG uMinorVersion;
    ULONG uNumOfTXBuffers;
    ULONG uNumOfRXBuffers;
    ULONG uOpModeCapability;
} DOT11_OPERATION_MODE_CAPABILITY, * PDOT11_OPERATION_MODE_CAPABILITY;
```

## <span id="OID_DOT11_CURRENT_OPERATION_MODE"></span><span id="oid_dot11_current_operation_mode"></span>OID\_DOT11\_CURRENT\_OPERATION\_MODE


The **OID\_DOT11\_CURRENT\_OPERATION\_MODE** command can be called in either set or query mode to configure or return the driver’s current operation mode.

This command functions as previously documented, but the driver is now required to support the **DOT11\_OPERATION\_MODE\_MANUFACTURING** operation mode. For complete documentation of this OID, see [OID\_DOT11\_CURRENT\_OPERATION\_MODE](https://msdn.microsoft.com/library/windows/hardware/ff569132) on MSDN.

``` syntax
typedef struct _DOT11_CURRENT_OPERATION_MODE {
    ULONG uReserved;
    ULONG uCurrentOpMode;
} DOT11_CURRENT_OPERATION_MODE, * PDOT11_CURRENT_OPERATION_MODE; 
```

<span id="uCurrentOpMode"></span><span id="ucurrentopmode"></span><span id="UCURRENTOPMODE"></span>*uCurrentOpMode*  
\[in\] Specifies the driver operation mode to be set. This parameter also functions as a placeholder for the driver to return the operation mode when called in query mode. If the driver does not support the requested operation mode, it should return **NDIS\_STATUS\_BAD\_VERSION**.

## <span id="related_topics"></span>Related topics


[Adding Wi-Fi manufacturing test support to the OID interface](adding-wi-fi-manufacturing-test-support-to-the-oid-interface.md)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bp_phManuRetail\p_phManuRetail%5D:%20Supporting%20updated%20OID%20behavior%20in%20manufacturing%20mode%20%20RELEASE:%20%284/11/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")



