---
description: La \_ classe WMI dell'associazione ShareToDirectory Win32 mette in correlazione una risorsa condivisa nel computer e la directory a cui viene mappata.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Classe Win32_ShareToDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747823"
---
# <a name="win32_sharetodirectory-class"></a>Win32 \_ ShareToDirectory (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ ShareToDirectory Win32** mette in correlazione una risorsa condivisa nel computer e la directory a cui viene mappata.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ ShareToDirectory** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ ShareToDirectory** dispone di queste proprietà.

<dl> <dt>

**Condividi**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ condivisione Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| condivisione Win32 WMI \_ ")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà di una risorsa condivisa disponibile tramite la directory.

</dd> <dt>

**SharedElement**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ directory CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ directory")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà della directory di cui è stato eseguito il mapping a una risorsa condivisa.

</dd> </dl>

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

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
