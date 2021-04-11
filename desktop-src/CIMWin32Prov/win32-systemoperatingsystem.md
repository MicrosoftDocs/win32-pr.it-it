---
description: La \_ classe WMI dell'associazione SystemOperatingSystem Win32 mette in correlazione un computer e il relativo sistema operativo.
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Classe Win32_SystemOperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba3f8ac94ec882ee1df96da51d93d2c24fde9b3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127610"
---
# <a name="win32_systemoperatingsystem-class"></a>Win32 \_ SystemOperatingSystem (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemOperatingSystem Win32** mette in correlazione un computer e il relativo sistema operativo.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SystemOperatingSystem** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SystemOperatingSystem** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

[**\_ ComputerSystem Win32**](win32-computersystemprocessor.md) che descrive le proprietà del computer su cui è installato il sistema operativo.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ OperatingSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")
</dt> </dl>

[**\_ OperatingSystem Win32**](win32-operatingsystem.md) che descrive le proprietà del sistema operativo in esecuzione nel computer.

</dd> <dt>

**Primarie**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sistema operativo DMTF \| 001,4 ")
</dt> </dl>

Se **true**, il sistema operativo installato è il sistema operativo predefinito per il computer.

Questa proprietà viene ereditata da [**CIM \_ installato**](cim-installedos.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ SystemOperatingSystem** è derivata da [**CIM \_ installato**](cim-installedos.md).

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

[**CIM \_ installato**](cim-installedos.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
