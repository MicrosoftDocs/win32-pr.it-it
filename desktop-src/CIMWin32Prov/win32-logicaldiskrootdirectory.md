---
description: La \_ classe WMI dell'associazione LogicalDiskRootDirectory Win32 mette in correlazione un disco logico e la relativa struttura di directory.
ms.assetid: 860cd28a-2a59-4ce3-be26-8fdc869c70d1
ms.tgt_platform: multiple
title: Classe Win32_LogicalDiskRootDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskRootDirectory
- Win32_LogicalDiskRootDirectory.GroupComponent
- Win32_LogicalDiskRootDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b015891a37c5cc92bbf102482f48306d537bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877269"
---
# <a name="win32_logicaldiskrootdirectory-class"></a>Win32 \_ LogicalDiskRootDirectory (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LogicalDiskRootDirectory Win32** mette in correlazione un disco logico e la relativa struttura di directory.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE468-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalDiskRootDirectory : CIM_Component
{
  Win32_LogicalDisk REF GroupComponent;
  Win32_Directory   REF PartComponent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ LogicalDiskRootDirectory** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ LogicalDiskRootDirectory** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ disco logico**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ disco logico")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà del disco logico.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ directory Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| directory Win32 WMI \_ ")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà della struttura di directory di file.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ LogicalDiskRootDirectory** è derivata dal [**\_ componente CIM**](cim-component.md).

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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

