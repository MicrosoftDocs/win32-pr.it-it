---
description: La proprietà DataSize dell'oggetto Record è una proprietà di sola lettura che restituisce le dimensioni dei dati per il campo designato.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Record.DataSize - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 067fc09e65d644413e75ccd8a9c0173e30df8060dff0f772ae5d12705ab610aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912961"
---
# <a name="recorddatasize-property"></a>Record.DataSize - proprietà

La **proprietà DataSize** dell'oggetto [**Record**](record-object.md) è una proprietà di sola lettura che restituisce le dimensioni dei dati per il campo designato. Se i dati sono un flusso, viene restituita la lunghezza del flusso in byte. Se i dati sono una stringa, viene restituita la lunghezza della stringa senza Null. Se i dati sono un numero intero, viene restituito il valore 4 (che indica le dimensioni dell'intero). Se i dati sono Null, viene restituito 0.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a>Valore proprietà

Numero di campo obbligatorio del valore all'interno del record, in base 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




