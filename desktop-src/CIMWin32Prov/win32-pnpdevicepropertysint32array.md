---
description: Rappresenta una proprietà del dispositivo PnP costituita da una matrice di elementi Sint32.
ms.assetid: 8CA6421B-6AC7-4590-9142-4093AA7BE019
ms.tgt_platform: multiple
title: Win32_PnPDevicePropertySint32Array classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevicePropertySint32Array
- Win32_PnPDevicePropertySint32Array.Key
- Win32_PnPDevicePropertySint32Array.KeyName
- Win32_PnPDevicePropertySint32Array.Type
- Win32_PnPDevicePropertySint32Array.DeviceID
- Win32_PnPDevicePropertySint32Array.Data
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3811907e08d5802b18fbfa81438ae3544f26094c1e3ae005dfa2642d6c2763c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118008817"
---
# <a name="win32_pnpdevicepropertysint32array-class"></a>Classe \_ Win32 PnPDevicePropertySint32Array

Rappresenta una proprietà del dispositivo PnP costituita da una matrice di **elementi Sint32.**

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_PnPDevicePropertySint32Array : Win32_PnPDeviceProperty
{
  string Key;
  string KeyName;
  Uint32 Type;
  string DeviceID;
  Sint32 Data[];
};
```

## <a name="members"></a>Members

La **classe Win32 \_ PnPDevicePropertySint32Array** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ PnPDevicePropertySint32Array** ha queste proprietà.

<dl> <dt>

**Dati**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice Sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore della proprietà.

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica il dispositivo PnP.

Questa proprietà viene ereditata da [**Win32 \_ PnPDeviceProperty.**](win32-pnpdeviceproperty.md)

</dd> <dt>

**Chiave**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore della coppia chiaveName-Value che identifica la **proprietà** Data.

Questa proprietà viene ereditata da [**Win32 \_ PnPDeviceProperty.**](win32-pnpdeviceproperty.md)

</dd> <dt>

**Keyname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della coppia chiaveName-Value che identifica la **proprietà** Data.

Questa proprietà viene ereditata da [**Win32 \_ PnPDeviceProperty.**](win32-pnpdeviceproperty.md)

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo della **proprietà Data.**

Questa proprietà viene ereditata da [**Win32 \_ PnPDeviceProperty.**](win32-pnpdeviceproperty.md)

I valori possibili sono .

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

**Vuoto** (0)


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

**Null** (1)


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

**SByte** (2)


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

**Byte** (3)


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

**Int16** (4)


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

**UInt16** (5)


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

**Int32** (6)


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

**Uint32** (7)


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

**Int64** (8)


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

**UInt64** (9)


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

**Float** (10)


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

**Double** (11)


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

**Decimal** (12)


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

**GUID** (13)


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

**Valuta** (14)


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

**Data** (15)


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

**FileTime** (16)


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

**Boolean** (17)


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

**Stringa** (18)


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

**SecurityDescriptor** (19)


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

**SecurityDescriptorString** (20)


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

**DEVPROPKEY** (21)


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

**DEVPROPTYPE** (22)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** (23)


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

**NTStatus** (24)


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

**StringIndirect** (25)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reserved**


</dt> <dd>26–4097</dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

**SByteArray** (4098)


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

**Binario** (4099)


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

**Int16Array** (4100)


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

**UInt16Array** (4101)


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

**Int64Array** (4102)


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

**UInt64Array** (4103)


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

**FloatArray** (4104)


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

**DoubleArray** (4105)


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

**DecimalArray** (4106)


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

**GuidArray** (4107)


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

**CurrencyArray** (4108)


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

**DateArray** (4109)


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

**FileTimeArray** (4110)


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

**BooleanArray** (4111)


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

**StringList** (4112)


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

**SecurityDescriptorList** (4113)


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

**SecurityDescriptorStringList** (8210)


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

**DEVPROPKEYArray** (8211)


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

**DEVPROPTYPEArray** (8212)


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

**ErrorArray** (4117)


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

**NTStatusArray** (4118)


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

**StringIndirectList** (4119)


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

**Sconosciuto: archiviare devpropdef.h** (4120)


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

**TBD** (8217)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reserved**


</dt> <dd>8218–4294967295</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md)
</dt> <dt>

[**GetDeviceProperties**](getdeviceproperties-win32-pnpentity.md)
</dt> </dl>

 

 




