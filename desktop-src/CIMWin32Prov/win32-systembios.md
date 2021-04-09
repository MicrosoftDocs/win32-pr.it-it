---
description: La \_ classe WMI dell'associazione SystemBIOS Win32 mette in relazione un computer (inclusi dati quali le proprietà di avvio, i fusi orari, le configurazioni di avvio o le password amministrative) e un BIOS di sistema (servizi, lingue e proprietà di gestione del sistema).
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Classe Win32_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc8ec1f3526e2faefe0e63c9dea357accd025c13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878218"
---
# <a name="win32_systembios-class"></a>Win32 \_ SystemBIOS (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemBIOS Win32** mette in relazione un computer (inclusi dati quali le proprietà di avvio, i fusi orari, le configurazioni di avvio o le password amministrative) e un BIOS di sistema (servizi, lingue e proprietà di gestione del sistema).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SystemBIOS** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SystemBIOS** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

[**\_ ComputerSystem Win32**](win32-computersystemprocessor.md) che contiene il BIOS dell'associazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ BIOS Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| BIOS Win32 Win32 \_ ")
</dt> </dl>

Un [**\_ BIOS Win32**](win32-bios.md) contenuto nel computer del sistema di questa associazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ SystemBIOS** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).

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

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
