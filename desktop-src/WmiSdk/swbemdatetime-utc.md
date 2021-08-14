---
description: Ottiene o imposta la rappresentazione UTC (Coordinated Universal Times) del valore datetime.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime.UTC (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c1bb3307116042a61aae06489bec7d8eabbf7859f3e8770811b50680dcfe5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314694"
---
# <a name="swbemdatetimeutc-property"></a>Proprietà SWbemDateTime.UTC

La **proprietà UTC** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) ottiene o imposta la rappresentazione UTC (Coordinated Universal Times) del **valore datetime.** UTC è l'ora impostata dal world time standard. L'ora UTC ha sostituito Greenwich Mean Time (GMT). Un valore UTC con offset zero è uguale a GMT con un offset zero. Il numero con segno deve essere compreso nell'intervallo compreso tra -720 e 720 oppure viene restituito l'errore **wbemErrValueOutOfRange.**

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a>Valore proprietà

## <a name="error-codes"></a>Codici di errore

Dopo aver ricevuto o impostato la **proprietà UTC,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore seguente.

<dl> <dt>

**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)
</dt> <dd>

Il valore non è compreso nell'intervallo compreso tra -720 e 720.

</dd> </dl>

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

[**SWbemDateTime.UTCSpecified**](swbemdatetime-utcspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

