---
description: Ottiene o imposta un valore che rappresenta il componente minuti del valore datetime.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime.Minutes (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5a6150dcdee6051fdfb8737618f4735cfe1e568da05ec35a6cd935be197a56ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992241"
---
# <a name="swbemdatetimeminutes-property"></a>Proprietà SWbemDateTime.Minutes

La **proprietà Minutes** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) ottiene o imposta un valore che rappresenta il componente minutes del valore datetime.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a>Valore proprietà

## <a name="error-codes"></a>Codici di errore

Dopo aver ottiene o impostato la **proprietà Minutes,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore seguente.

<dl> <dt>

**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)
</dt> <dd>

Il valore non è compreso nell'intervallo compreso tra 0 e 59.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la proprietà **SWbemDateTime.Minutes** è impostata su 1, la proprietà [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) contiene un valore che viene compensato di un secondo da un errore di arrotondamento che si verifica quando un valore **datetime** CIM viene convertito in un **valore VT \_ DATE.** Se invece **la proprietà Minutes** è impostata su 0, la proprietà **Seconds** restituisce il valore corretto.

## <a name="examples"></a>Esempio

Per esempi di utilizzo dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire i valori [**CIM DATETIME**](datetime.md) in e dal formato **FILETIME** o **VT \_ DATE,** vedere [Attività WMI:](wmi-tasks--dates-and-times.md)date e ore . Per una descrizione del formato CIM **DATETIME,** vedere [Formato di data e ora](date-and-time-format.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemDateTime.MinutesSpecified**](swbemdatetime-minutesspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

