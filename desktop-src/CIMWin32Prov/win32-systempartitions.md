---
description: La \_ classe WMI dell'associazione SystemPartitions Win32 mette in correlazione un computer e una partizione disco in tale sistema.
ms.assetid: e8f02cd0-9446-4258-b476-5dc6c72c80d4
ms.tgt_platform: multiple
title: Classe Win32_SystemPartitions
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
ms.openlocfilehash: deae8129772e5d854f05b5b953ec66a12bd5bcaf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877806"
---
# <a name="win32_systempartitions-class"></a>Win32 \_ SystemPartitions (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemPartitions Win32** mette in correlazione un computer e una partizione disco in tale sistema.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

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

La classe **Win32 \_ SystemPartitions** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SystemPartitions** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà del computer in cui si trova la partizione del disco.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ DiskPartition**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ DiskPartition")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà di una partizione disco esistente nel computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ SystemPartitions** è derivata da [**Win32 \_ SystemDevices**](win32-systemdevices.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SystemDevices Win32**](win32-systemdevices.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
