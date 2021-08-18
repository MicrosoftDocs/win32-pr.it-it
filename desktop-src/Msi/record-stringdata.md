---
description: La proprietà StringData dell'oggetto Record è una proprietà di lettura/scrittura che trasferisce i dati stringa da o verso un campo specificato all'interno del record. Se è stato archiviato un intero o un oggetto, viene restituito il relativo valore stringa.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Record.StringData - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3b789d8f4d8c6bf26c63c5313c61d95035bb130e4a57b63fbe9c12cdc141bb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327771"
---
# <a name="recordstringdata-property"></a>Record.StringData - proprietà

La **proprietà StringData** dell'oggetto [**Record**](record-object.md) è una proprietà di lettura/scrittura che trasferisce i dati stringa da o verso un campo specificato all'interno del record. Se è stato archiviato un intero o un oggetto, viene restituito il relativo valore stringa.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a>Valore proprietà

Numero di campo obbligatorio del valore all'interno del record, in base 1.

## <a name="remarks"></a>Commenti

Il valore restituito di un campo inesistente è una stringa vuota. Per impostare un campo della stringa di record su Null, usare una variante vuota o una stringa vuota. Il tentativo di archiviare un valore in un campo inesistente causa un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




