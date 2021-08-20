---
description: Valore booleano che indica se il componente microsecondi nel valore datetime CIM contiene un intervallo o un valore con caratteri jolly.
ms.assetid: 65244ece-2326-4edc-b982-57e2046ec33e
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime.MicrosecondsSpecified (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.get_MicrosecondsSpecified
- ISWbemDateTime.put_MicrosecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1b516b5fbe98c8bf481eaeed5b01c11f2dde6697a5832afc9d505d49254db2a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816379"
---
# <a name="swbemdatetimemicrosecondsspecified-property"></a>SWbemDateTime.MicrosecondsSpecified - proprietà

La proprietà **MicrosecondsSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente microsecondi nel valore datetime CIM contiene un intervallo o un valore con caratteri jolly. Se **MicrosecondsSpecified** è **TRUE** e [**IsInterval**](swbemdatetime-isinterval.md) è **FALSE,** [**SWbemDateTime.Microseconds**](swbemdatetime-microseconds.md) contiene un valore datetime. Un valore datetime che contiene un intervallo non può essere convertito nel formato **\_ VT DATE** o **FILETIME.** Se [**HoursSpecified**](swbemdatetime-hoursspecified.md) è **FALSE** e **IsInterval** è **TRUE,** **SWbemDateTime.Microseconds** contiene un intervallo.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.MicrosecondsSpecified As Boolean
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

[**SWbemDateTime.Microseconds**](swbemdatetime-microseconds.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




