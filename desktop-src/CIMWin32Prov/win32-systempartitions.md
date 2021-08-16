---
description: La classe WMI di associazione Win32 SystemPartitions mette in relazione un sistema di computer e una partizione \_ del disco in tale sistema.
ms.assetid: e8f02cd0-9446-4258-b476-5dc6c72c80d4
ms.tgt_platform: multiple
title: Win32_SystemPartitions classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemPartitions
- Win32_SystemPartitions.GroupComponent
- Win32_SystemPartitions.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c5ec2682e6a81d0cdc3e9fa590418bdf03e46c0a60086b470cd8bc4c97006fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833949"
---
# <a name="win32_systempartitions-class"></a>Classe \_ SystemPartitions Win32

La classe [WMI](../wmisdk/retrieving-a-class.md) **di associazione Win32 \_ SystemPartitions** mette in relazione un sistema di computer e una partizione del disco in tale sistema.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemPartitions : Win32_SystemDevices
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_DiskPartition  REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ SystemPartitions Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SystemPartitions Win32** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ ComputerSystem Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("ComputerSystem \| Win32 \_ WMI")
</dt> </dl>

Riferimento all'istanza che rappresenta le proprietà del computer in cui si trova la partizione del disco.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ DiskPartition**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ DiskPartition")
</dt> </dl>

Riferimento all'istanza che rappresenta le proprietà di una partizione del disco presente nel sistema del computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ SystemPartitions Win32** è derivata da [**\_ SystemDevices Win32.**](win32-systemdevices.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sistema \_ Win32Dispositori**](win32-systemdevices.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
