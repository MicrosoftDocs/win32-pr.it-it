---
description: Valore booleano che indica se il componente secondi nel valore DATETIME CIM contiene un intervallo o un valore jolly.
ms.assetid: 9f9b75c3-ae08-49a6-b747-294831601a62
ms.tgt_platform: multiple
title: Proprietà SWbemDateTime. SecondsSpecified (wbemdisp. h)
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
ms.openlocfilehash: e0cf97eff544d6e244890014108506f39b1934b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885033"
---
# <a name="swbemdatetimesecondsspecified-property"></a>Proprietà SWbemDateTime. SecondsSpecified

La proprietà **SecondsSpecified** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) è un valore booleano che indica se il componente secondi nel valore [**DateTime**](datetime.md) CIM contiene un intervallo o un valore jolly. Se **SecondsSpecified** è **true** e l' [**intervallo**](swbemdatetime-isinterval.md) è **false**, [**SWbemDateTime. seconds**](swbemdatetime-seconds.md) contiene un valore di data. Un valore DateTime che contiene un intervallo non può essere convertito nel formato **di \_ Data VT** o nel formato **FILETIME** . Se **SecondsSpecified** è **false** e l' **intervallo** è **true**, **SWbemDateTime. seconds** contiene un intervallo.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.SecondsSpecified As Boolean
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

[**SWbemDateTime. secondi**](swbemdatetime-seconds.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




