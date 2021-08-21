---
description: Valore booleano che indica se il componente secondi nel valore CIM DATETIME contiene un intervallo o un valore con caratteri jolly.
ms.assetid: 9f9b75c3-ae08-49a6-b747-294831601a62
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime.SecondsSpecified (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SecondsSpecified
- ISWbemDateTime.SecondsSpecified
- ISWbemDateTime.get_SecondsSpecified
- ISWbemDateTime.put_SecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 54c90d5f719a4e25464dca5389bb5721919edffa8ee14f79f6902d438280bd30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816261"
---
# <a name="swbemdatetimesecondsspecified-property"></a>SWbemDateTime.SecondsSpecified - proprietà

La **proprietà SecondsSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente secondi nel valore CIM [**DATETIME**](datetime.md) contiene un intervallo o un valore con caratteri jolly. Se **SecondsSpecified è** **TRUE** e [**IsInterval**](swbemdatetime-isinterval.md) è **FALSE,** [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) contiene un valore di data. Un valore datetime che contiene un intervallo non può essere convertito nel formato **\_ VT DATE** o **FILETIME.** Se **SecondsSpecified è** **FALSE** e **IsInterval** è **TRUE,** **SWbemDateTime.Seconds** contiene un intervallo.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.SecondsSpecified As Boolean
```



## <a name="property-value"></a>Valore proprietà

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

[**SWbemDateTime.Seconds**](swbemdatetime-seconds.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




