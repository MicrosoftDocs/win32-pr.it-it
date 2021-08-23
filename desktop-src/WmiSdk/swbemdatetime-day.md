---
description: Ottiene o imposta un valore che rappresenta il componente giorno del valore datetime.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime.Day (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d2483e52d9b40978a28f96bb5352df4f9abf4f89becf52550b82fd931580d7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640501"
---
# <a name="swbemdatetimeday-property"></a>SWbemDateTime.Day - proprietà

La **proprietà Day** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) ottiene o imposta un valore che rappresenta il componente giorno del valore datetime. Se [**IsInterval**](swbemdatetime-isinterval.md) è **FALSE,** il valore deve essere compreso tra 1 e 31. Tuttavia, il controllo degli errori non è sensibile al valore del mese. Pertanto, il valore compreso nell'intervallo 31 non restituirà un errore nei casi in cui il [**valore SWbemDateTime.Month**](swbemdatetime-month.md) è per un mese di meno di 31 giorni (febbraio, aprile, giugno, settembre, novembre).

Il valore predefinito per **Day** è 01.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a>Valore proprietà

## <a name="error-codes"></a>Codici di errore

Dopo aver ottiene o impostato la **proprietà Day,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore seguente.

<dl> <dt>

**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)
</dt> <dd>

Se [**IsInterval**](swbemdatetime-isinterval.md) è **TRUE** e l'intervallo di valori corretti è compreso tra 0 e 99999999.

</dd> </dl>

## <a name="examples"></a>Esempio

Per esempi d'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire i valori [**CIM DATETIME**](datetime.md) nel e dal formato **FILETIME** o **VT \_ DATE,** vedere [Attività WMI:](wmi-tasks--dates-and-times.md)date e ore. Per una descrizione del formato **CIM DATETIME,** vedere [Formato di data e ora.](date-and-time-format.md)

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

[**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

