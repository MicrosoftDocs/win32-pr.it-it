---
description: La classe WMI di associazione SystemBIOS Win32 mette in relazione un sistema informatico (inclusi dati come proprietà di avvio, fusi orari, configurazioni di avvio o password amministrative) e un BIOS di sistema (servizi, lingue e proprietà di gestione del \_ sistema).
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Win32_SystemBIOS classe
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
ms.openlocfilehash: c9180b78add8b2646ae39a6f910296d53499e513f4fa05a4bbaaee42e240de5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971507"
---
# <a name="win32_systembios-class"></a>Classe \_ SystemBIOS Win32

La classe [WMI](../wmisdk/retrieving-a-class.md) di associazione **\_ SystemBIOS Win32** mette in relazione un sistema informatico (inclusi dati come proprietà di avvio, fusi orari, configurazioni di avvio o password amministrative) e un BIOS di sistema (servizi, lingue e proprietà di gestione del sistema).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe \_ SystemBIOS Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SystemBIOS Win32** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ ComputerSystem Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Wmi \| Win32 \_ ComputerSystem")
</dt> </dl>

Oggetto [**\_ ComputerSystem Win32**](win32-computersystemprocessor.md) contenente il BIOS dell'associazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ BIOS Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("BIOS \| Win32 \_ WMI")
</dt> </dl>

BioS [**Win32 \_**](win32-bios.md) contenuto nel sistema informatico di questa associazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ SystemBIOS Win32** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).

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

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

 
