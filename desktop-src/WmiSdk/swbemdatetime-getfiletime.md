---
description: Converte un valore di data e ora nel formato CIM DATETIME nel formato FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Metodo SWbemDateTime.GetFileTime (Wbemdisp.h)
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
ms.openlocfilehash: 8c35daf5b6e986b2519f127969edc5bbcf05a260bd23e8aa1168b1a7c20a5372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739438"
---
# <a name="swbemdatetimegetfiletime-method"></a>Metodo SWbemDateTime.GetFileTime

Il **metodo GetFileTime** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte un valore di data e ora nel formato CIM [DATETIME](datetime.md) nel formato FILETIME.

Se il parametro è impostato su **TRUE,** il valore restituito rappresenta un'ora locale per il client. In caso contrario, il valore restituito è Coordinated Universal Time (UTC). Una struttura **FILETIME** [DATETIME](datetime.md) è un valore a 64 bit che rappresenta il numero di unità da 100 nanosecondi dall'inizio del 1° gennaio 1601. Windows Strumentazione gestione (WMI) considera i **valori FILETIME** come rappresentazioni di stringa di numeri a 64 bit senza segno.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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

Indica se il valore restituito viene interpretato come ora locale. La proprietà UTC contiene quindi l'ora locale convertita nell'offset UTC (Coordinated Universal Time) corretto. Se il valore è **FALSE,** il valore viene interpretato come UTC con un offset zero (0).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Data e ora nel **formato FILETIME.**

## <a name="error-codes"></a>Codici di errore

Dopo aver completato il **metodo GetFileTime,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

La chiamata non è riuscita.

</dd> </dl>

## <a name="remarks"></a>Commenti

**VT \_ I valori DATE** **e FILETIME non** possono contenere campi con caratteri jolly.

Il **metodo GetFileTime** ha esito negativo (wbemErrFailed) se una delle proprietà seguenti è **FALSE**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondiSpecificato**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondiSpecificati**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecificato**](swbemdatetime-utcspecified.md)

In caso di esito positivo restituito da [**SetFileTime,**](swbemdatetime-setfiletime.md)tutte queste proprietà sono impostate su **TRUE.**

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

[**SWbemDateTime.GetVarDate**](swbemdatetime-getvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

