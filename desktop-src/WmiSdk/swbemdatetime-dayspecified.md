---
description: Valore booleano che indica se il componente giorno nel valore DATETIME CIM contiene un intervallo o un valore con caratteri jolly.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime.DaySpecified (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: effa3bcb68351aa754006c143e738443efdb7238129f30847876ad17527ca279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992251"
---
# <a name="swbemdatetimedayspecified-property"></a>SWbemDateTime.DaySpecified - proprietà

La **proprietà DaySpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente giorno nel valore [**DATETIME**](datetime.md) CIM contiene un intervallo o un valore con caratteri jolly. Se **DaySpecified** è **TRUE** e [**IsInterval**](swbemdatetime-isinterval.md) è **FALSE,** [**SWbemDateTime.Day**](swbemdatetime-day.md) contiene un valore datetime. Un [**valore DATETIME**](datetime.md) che contiene un intervallo non può essere convertito nel formato **\_ VT DATE** o **FILETIME.** Se **DaySpecified** è **FALSE** e **IsInterval** è **TRUE,** **SWbemDateTime.Day** contiene un intervallo.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.DaySpecified As BOOLEAN
```



## <a name="property-value"></a>Valore proprietà

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

[**SWbemDateTime.Day**](swbemdatetime-day.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

 




