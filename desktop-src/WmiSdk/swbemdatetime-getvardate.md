---
description: Converte un valore di data e ora nel formato CIM DATETIME nel formato \_ VT DATE.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Metodo SWbemDateTime.GetVarDate (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 506c897da130b9558b37637918674a7c6024adb787ac3d91e53e430a6edfcd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314756"
---
# <a name="swbemdatetimegetvardate-method"></a>Metodo SWbemDateTime.GetVarDate

Il **metodo GetVarDate** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte un valore di data e ora nel formato [**CIM DATETIME**](datetime.md) nel **formato \_ VT DATE.**

Il **formato VT \_ DATE** è un valore [**DATETIME**](datetime.md) della variante di automazione che Visual Basic e ActiveX usare.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bIsLocal* \[ in, facoltativo\]
</dt> <dd>

Indica se il valore restituito viene interpretato come ora locale. La Coordinated Universal Time (UTC) contiene l'ora locale convertita nell'offset UTC corretto. Se il valore è **FALSE,** il valore viene interpretato come UTC con un offset zero (0).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore di data e ora nel **formato \_ VT DATE.**

## <a name="remarks"></a>Commenti

**VT \_ I valori DATE** e **FILETIME** non possono contenere campi con caratteri jolly.

Il **metodo GetVarDate** ha esito negativo (**wbemErrFailed**) se una delle proprietà seguenti è **FALSE**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondiSpecificati**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

In caso di esito positivo [**restituito da SetVarDate,**](swbemdatetime-setvardate.md)tutte queste proprietà vengono impostate su **TRUE.**

Dopo una chiamata riuscita a [**SetVarDate,**](swbemdatetime-setvardate.md)il valore [**DATETIME**](datetime.md) viene sempre interpretato come un valore **DATETIME** assoluto anziché come un intervallo e [**IsInterval**](swbemdatetime-isinterval.md) è impostato su **FALSE.**

Se [**IsInterval**](swbemdatetime-isinterval.md) è impostato su **TRUE,** una chiamata a **GetVarDate** restituisce l'errore **wbemErrFailed.**

Si verifica una perdita di precisione quando si chiama **GetVarDate**, perché i valori [datetime](datetime.md) hanno una risoluzione di un microsecondo (s) e i valori **\_ VT DATE** hanno una risoluzione di 500 millisecondi.

## <a name="examples"></a>Esempio

Per esempi d'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire i valori [**DATETIME**](datetime.md) CIM in e dal formato **FILETIME** o **VT \_ DATE,** vedere [Wmi Tasks: Dates and Times](wmi-tasks--dates-and-times.md). Per una descrizione del formato **CIM DATETIME,** vedere [Formato di data e ora.](date-and-time-format.md)

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

[**SWbemDateTime.GetFileTime**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




