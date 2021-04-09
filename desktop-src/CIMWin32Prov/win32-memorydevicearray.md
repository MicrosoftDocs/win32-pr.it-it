---
description: La \_ classe WMI dell'associazione MemoryDeviceArray Win32 mette in correlazione un dispositivo di memoria e la matrice di memoria in cui risiede.
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Classe Win32_MemoryDeviceArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceArray
- Win32_MemoryDeviceArray.GroupComponent
- Win32_MemoryDeviceArray.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e527f77183c3bdc09d464f6fed4808e45adefa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877341"
---
# <a name="win32_memorydevicearray-class"></a>Win32 \_ MemoryDeviceArray (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ MemoryDeviceArray Win32** mette in correlazione un dispositivo di memoria e la matrice di memoria in cui risiede.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF563-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryDeviceArray : CIM_Component
{
  Win32_MemoryArray  REF GroupComponent;
  Win32_MemoryDevice REF PartComponent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ MemoryDeviceArray** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ MemoryDeviceArray** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ MemoryArray**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")
</dt> </dl>

[**\_ MemoryArray Win32**](win32-memoryarray.md) che rappresenta la parte della matrice di memoria dell' \_ associazione MemoryDeviceArray Win32.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ MemoryDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")
</dt> </dl>

[**\_ MemoryDevice Win32**](win32-memorydevice.md) che rappresenta una parte del dispositivo di memoria dell' \_ associazione MemoryDeviceArray Win32.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ MemoryDeviceArray** è derivata dal [**\_ componente CIM**](cim-component.md).

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

[**\_Componente CIM**](cim-component.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

