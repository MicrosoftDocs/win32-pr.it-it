---
description: Valore booleano che indica se il componente month nel valore datetime CIM contiene un intervallo o un valore con caratteri jolly.
ms.assetid: 12dd94de-24be-4b13-bde5-2fc28be94efa
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime.MonthSpecified (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MonthSpecified
- ISWbemDateTime.MonthSpecified
- ISWbemDateTime.get_MonthSpecified
- ISWbemDateTime.put_MonthSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fa0ab9d3107f0374228b8c8edcda4ecffc4744cf4ef52b8a019e6ca4c8138f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992171"
---
# <a name="swbemdatetimemonthspecified-property"></a>SWbemDateTime.MonthSpecified - proprietà

La **proprietà MonthSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente month nel valore datetime CIM contiene un intervallo o un valore con caratteri jolly. Se **MonthSpecified è** **TRUE** e [**IsInterval**](swbemdatetime-isinterval.md) è **FALSE,** [**SWbemDateTime.Month**](swbemdatetime-month.md) contiene un valore di data. Un valore datetime che contiene un intervallo non può essere convertito nel formato **VT \_ DATE** o **FILETIME.** Se **MonthSpecified è** **FALSE** e **IsInterval** è **TRUE,** **SWbemDateTime.Month** contiene un intervallo.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.MonthSpecified As Boolean
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

[**SWbemDateTime.Month**](swbemdatetime-month.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




