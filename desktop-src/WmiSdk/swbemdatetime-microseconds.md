---
description: Ottiene o imposta un valore che rappresenta il componente microsecondi del valore DateTime.
ms.assetid: b810b781-86a3-4730-8114-44d10454f7c3
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. microsecondi (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Microseconds
- ISWbemDateTime.Microseconds
- ISWbemDateTime.get_Microseconds
- ISWbemDateTime.put_Microseconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 94213eb70a98be1af8f8404ddece8bf2f07ca807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349621"
---
# <a name="swbemdatetimemicroseconds-property"></a>Proprietà SWbemDateTime. microsecondi

La proprietà **microsecondi** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) Ottiene o imposta un valore che rappresenta il componente microsecondi del valore DateTime.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.Microseconds As Long
```



## <a name="property-value"></a>Valore proprietà

## <a name="error-codes"></a>Codici di errore

Dopo avere ottenuto o impostato la proprietà **microsecondi** , l'oggetto **Err** può contenere il codice di errore riportato di seguito.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B)
</dt> <dd>

Il valore non è compreso nell'intervallo tra 0 e 999999.

</dd> </dl>

## <a name="examples"></a>Esempio

Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md). Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMDATETIME CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMDATETIME IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemDateTime. MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

 




