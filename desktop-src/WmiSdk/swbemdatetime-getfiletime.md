---
description: Converte un valore di data e ora nel formato DATETIME CIM nel formato FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Metodo SWbemDateTime. GetFileTime ha provocato (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485732"
---
# <a name="swbemdatetimegetfiletime-method"></a>SWbemDateTime. GetFileTime ha provocato, metodo

Il metodo **GetFileTime ha provocato** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte un valore di data e ora nel formato [DateTime](datetime.md) CIM nel formato FILETIME.

Se il parametro è impostato su **true**, il valore restituito rappresenta un'ora locale per il client. In caso contrario, il valore restituito è un'ora UTC (Coordinated Universal Time). Una struttura [DateTime](datetime.md) **FILETIME** è un valore a 64 bit che rappresenta il numero di unità 100-nanosecondi a partire dall'inizio del 1 ° gennaio 1601. Strumentazione gestione Windows (WMI) considera i valori **FILETIME** come rappresentazioni di stringa di numeri senza segno a 64 bit.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bIsLocaL* \[ in, facoltativo\]
</dt> <dd>

Indica se il valore restituito viene interpretato come ora locale. La proprietà UTC contiene quindi l'ora locale convertita nell'offset UTC (Coordinated Universal Time) corretto. Se il valore è **false**, il valore viene interpretato come UTC con un offset zero (0).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Data e ora nel formato **FILETIME** .

## <a name="error-codes"></a>Codici di errore

Dopo aver completato il metodo **GetFileTime ha provocato** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

La chiamata non è riuscita.

</dd> </dl>

## <a name="remarks"></a>Commenti

**VT \_** I valori di data e **FILETIME** non possono contenere campi con caratteri jolly.

Il metodo **GetFileTime ha provocato** ha esito negativo (wbemErrFailed) se una delle proprietà seguenti è **false**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

In seguito al corretto ritorno da [**SetFileTime**](swbemdatetime-setfiletime.md), tutte queste proprietà sono impostate su **true**.

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

[**SWbemDateTime. GetVarDate**](swbemdatetime-getvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

