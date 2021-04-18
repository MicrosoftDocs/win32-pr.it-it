---
description: Converte un valore di data e ora nel formato DATETIME CIM nel formato di \_ Data VT.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Metodo SWbemDateTime. GetVarDate (wbemdisp. h)
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
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309869"
---
# <a name="swbemdatetimegetvardate-method"></a>SWbemDateTime. GetVarDate, metodo

Il metodo **getVarDate** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte un valore di data e ora nel formato [**DateTime**](datetime.md) CIM nel formato **\_ Data VT** .

Il formato della **\_ Data VT** è un valore [**DateTime**](datetime.md) della variante di automazione che Visual Basic e ActiveX usano.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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

Indica se il valore restituito viene interpretato come ora locale. La proprietà UTC (Coordinated Universal Time) contiene l'ora locale convertita nell'offset UTC corretto. Se il valore è **false**, il valore viene interpretato come UTC con un offset zero (0).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore di data e ora nel formato **di \_ Data VT** .

## <a name="remarks"></a>Commenti

**VT \_** I valori di data e **FILETIME** non possono contenere campi con caratteri jolly.

Il metodo **getVarDate** ha esito negativo (**wbemErrFailed**) se una delle proprietà seguenti è **false**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

In seguito all'esito positivo della restituzione da [**SetVarDate**](swbemdatetime-setvardate.md), tutte queste proprietà vengono impostate su **true**.

Al termine di una chiamata a [**SetVarDate**](swbemdatetime-setvardate.md), il valore [**DateTime**](datetime.md) viene sempre interpretato come valore **DateTime** assoluto anziché come intervallo e l' [**intervallo**](swbemdatetime-isinterval.md) è impostato su **false**.

Se l' [**intervallo**](swbemdatetime-isinterval.md) è impostato su **true**, una chiamata a **getVarDate** genera l'errore **wbemErrFailed** .

Quando si chiama **getVarDate**, si verifica una perdita di precisione, perché i valori [DateTime](datetime.md) hanno una risoluzione di un microsecondo (s) e i valori di **\_ data VT** hanno una risoluzione di 500 millisecondi.

## <a name="examples"></a>Esempio

Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e da **FILETIME** o dal formato **di \_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md). Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).

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

[**SWbemDateTime. GetFileTime ha provocato**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




