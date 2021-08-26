---
description: La classe WMI di associazione Win32 ShareToDirectory mette in relazione una risorsa condivisa nel sistema del computer e la directory a \_ cui è mappata.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Win32_ShareToDirectory classe
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
ms.openlocfilehash: d041209dcdbd1d9a39d08acb75180ec9cf292f01934c21762418571d44a32460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917541"
---
# <a name="win32_sharetodirectory-class"></a>Classe \_ Win32 ShareToDirectory

La classe [WMI](../wmisdk/retrieving-a-class.md) di associazione **\_ Win32 ShareToDirectory** mette in relazione una risorsa condivisa nel sistema del computer e la directory a cui è mappata.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

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

La **classe Win32 \_ ShareToDirectory** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ ShareToDirectory** ha queste proprietà.

<dl> <dt>

**Condividi**
</dt> <dd> <dl> <dt>

Tipo di dati: **Condivisione Win32 \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Condivisione \| Win32 \_ WMI")
</dt> </dl>

Riferimento all'istanza che rappresenta le proprietà di una risorsa condivisa disponibile tramite la directory.

</dd> <dt>

**SharedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ Directory CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) \| ("CIM CIM \_ Directory")
</dt> </dl>

Riferimento all'istanza che rappresenta le proprietà della directory di cui è stato eseguito il mapping a una risorsa condivisa.

</dd> </dl>

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

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
