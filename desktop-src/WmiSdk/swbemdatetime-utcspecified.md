---
description: Valore booleano che indica se il componente UTC (Universal Coordinated Time) nel valore datetime CIM contiene un intervallo o un valore con caratteri jolly.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime.UTCSpecified (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80c8ab92d07c2ef75ea57a66f6bae26c428780e15beeae31c9e5bd883407f03f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640371"
---
# <a name="swbemdatetimeutcspecified-property"></a>SWbemDateTime.UTCSpecified - proprietà

La proprietà **UTCSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente UTC (Universal Coordinated Time) nel valore datetime CIM contiene un intervallo o un valore con caratteri jolly. Se **UTCSpecified** è **TRUE** e [**IsInterval**](swbemdatetime-isinterval.md) è **FALSE,** [**SWbemDateTime.UTC**](swbemdatetime-utc.md) contiene un [**valore DATETIME.**](datetime.md) Un **valore DATETIME** che contiene un intervallo non può essere convertito nel formato **\_ VT DATE** o **FILETIME.** Se **UTCSpecified** è **FALSE** e **IsInterval** è **TRUE,** **SWbemDateTime.UTC** contiene un intervallo.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a>Valore proprietà

## <a name="examples"></a>Esempio

Per esempi d'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire i valori [**CIM DATETIME**](datetime.md) nel e dal formato **FILETIME** o **VT \_ DATE,** vedere [Attività WMI:](wmi-tasks--dates-and-times.md)date e ore. Per una descrizione del formato datetime CIM, vedere [Formato di data e ora.](date-and-time-format.md)

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

[**SWbemDateTime.UTC**](swbemdatetime-utc.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




