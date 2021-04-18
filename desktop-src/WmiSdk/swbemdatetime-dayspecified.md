---
description: Valore booleano che indica se il componente relativo al giorno nel valore DATETIME CIM contiene un intervallo o un valore jolly.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. DaySpecified (wbemdisp. h)
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
ms.openlocfilehash: f295d33940f36212fde4fe821af8d5df24d4f75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309871"
---
# <a name="swbemdatetimedayspecified-property"></a>Proprietà SWbemDateTime. DaySpecified

La proprietà **DaySpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente relativo al giorno nel valore [**DateTime**](datetime.md) CIM contiene un intervallo o un valore jolly. Se **DaySpecified** è **true** e l' [**intervallo**](swbemdatetime-isinterval.md) è **false**, [**SWbemDateTime. Day**](swbemdatetime-day.md) contiene un valore DateTime. Un valore [**DateTime**](datetime.md) che contiene un intervallo non può essere convertito nel formato **di \_ Data VT** o nel formato **FILETIME** . Se **DaySpecified** è **false** e l' **intervallo** è **true**, **SWbemDateTime. Day** contiene un intervallo.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.DaySpecified As BOOLEAN
```



## <a name="property-value"></a>Valore proprietà

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

[**SWbemDateTime. giorno**](swbemdatetime-day.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

 




