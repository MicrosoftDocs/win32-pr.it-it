---
description: Rappresenta un intervallo contiguo di blocchi logici identificabili da un file system tramite il campo DeviceID (chiave) dei dischi.
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: CIM_LogicalDisk classe (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0fccc6600e0eb5f04fd7d00360402ad85a94746e55781acbd6b1a35c7f9b94fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812106"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a>CIM_LogicalDisk classe (gestione Hyper-V)

Rappresenta un intervallo contiguo di blocchi logici identificabili da un file system tramite il campo **DeviceID** (chiave) del disco. Ad esempio, in un ambiente Windows, il **campo DeviceID** contiene una lettera di unità. in un UNIX, contiene il percorso di accesso. e in un ambiente NetWare contiene il nome del volume.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a>Members

La **classe CIM \_ LogicalDisk** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ LogicalDisk** ha queste proprietà.

<dl> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")
</dt> </dl>

Indica se il dispositivo logico usa il formato del nome del sistema operativo.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

**Nome dispositivo del sistema operativo** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**NameNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")
</dt> </dl>

Indica se il dispositivo logico ha lo stesso spazio dei nomi del sistema operativo.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Spazio dei nomi del dispositivo del sistema** operativo (8)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ StorageExtent**](cim-storageextent.md)
</dt> </dl>

 

