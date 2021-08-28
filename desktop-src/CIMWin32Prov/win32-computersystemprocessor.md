---
description: La classe WMI di associazione ComputerSystemProcessor Win32 mette in relazione un \_ computer e un processore in esecuzione in tale sistema.
ms.assetid: e630ebea-19bf-43c7-a8a0-7acfda3a752b
ms.tgt_platform: multiple
title: Win32_ComputerSystemProcessor classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProcessor
- Win32_ComputerSystemProcessor.PartComponent
- Win32_ComputerSystemProcessor.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bfaf26800a9cb75052699fcd44076f67553a4a36df0c8597b5c9c6e2855d7370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417723"
---
# <a name="win32_computersystemprocessor-class"></a>Classe ComputerSystemProcessor Win32 \_

La classe WMI **di associazione \_ ComputerSystemProcessor Win32** mette in relazione un computer e un processore in esecuzione in tale sistema. [](/windows/desktop/WmiSdk/retrieving-a-class)

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{719A6839-C124-11d2-85E8-0000F8102E5F}"), AMENDMENT]
class Win32_ComputerSystemProcessor : Win32_SystemDevices
{
  Win32_Processor      REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a>Members

La **classe \_ ComputerSystemProcessor Win32** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ComputerSystemProcessor Win32** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ ComputerSystem Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("ComputerSystem \| Win32 \_ WMI")
</dt> </dl>

Oggetto **\_ ComputerSystem Win32** che descrive le proprietà del computer in cui è in esecuzione il processore.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Processore Win32 \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Processore \| Wmi Win32") \_
</dt> </dl>

Processore [**Win32 \_ che**](win32-processor.md) descrive le proprietà di un processore che esegue il computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ ComputerSystemProcessor Win32** è derivata da [**\_ SystemDevices Win32.**](win32-systemdevices.md)

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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

