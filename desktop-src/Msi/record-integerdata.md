---
description: Si tratta della proprietà IntegerData dell'oggetto Record. Questa proprietà di lettura/scrittura trasferisce i dati integer a 32 bit da o verso un campo specificato all'interno del record. Se non è possibile convertire un valore di campo in un numero intero, viene restituito msiDatabaseNullInteger.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Record.IntegerData - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3593f31d8f8cea6278346e8c99bb9c9b880aed273ae7ab70614ade112cd8c8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912921"
---
# <a name="recordintegerdata-property"></a>Record.IntegerData - proprietà

Si tratta della **proprietà IntegerData** dell'oggetto [**Record.**](record-object.md) Questa proprietà di lettura/scrittura trasferisce i dati integer a 32 bit da o verso un campo specificato all'interno del record. Se non è possibile convertire un valore di campo in un numero intero, viene restituito msiDatabaseNullInteger.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a>Valore proprietà

Numero di campo obbligatorio del valore all'interno del record, in base 1.

## <a name="remarks"></a>Commenti

Per impostare un campo intero di record su Null, usare msiDatabaseNullInteger. Il valore restituito di un campo inesistente è msiDatabaseNullInteger. Il tentativo di archiviare un valore in un campo inesistente causa un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




