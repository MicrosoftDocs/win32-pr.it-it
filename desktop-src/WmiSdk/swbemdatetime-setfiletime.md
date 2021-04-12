---
description: Converte una data nel formato della stringa FILETIME nel formato DateTime CIM.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Metodo SWbemDateTime. SetFileTime (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130994"
---
# <a name="swbemdatetimesetfiletime-method"></a>SWbemDateTime. SetFileTime, metodo

Il metodo **SetFileTime** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte una data nel formato della stringa **FILETIME** nel formato [DateTime CIM](date-and-time-format.md) .

Il formato **FILETIME** è una struttura datetime a 64 bit che rappresenta il numero di unità 100-nanosecondi a partire dall'inizio del 1 ° gennaio 1601. Strumentazione gestione Windows (WMI) considera i valori **FILETIME** come rappresentazioni di stringa di numeri senza segno a 64 bit.

Per la spiegazione della sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strFileTime* \[ in\]
</dt> <dd>

Valore **FILETIME** utilizzato per impostare l'oggetto.

</dd> <dt>

*bIsLocal* \[ in, facoltativo\]
</dt> <dd>

Se è **true**, *strFileTime* viene interpretato come ora locale. La proprietà UTC (Coordinated Universal Time) contiene l'ora locale convertita nell'offset UTC corretto. Quando *bIsLocal* è **false**, *strFileTime* viene convertito direttamente in un valore UTC con un offset di 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo aver completato il metodo **SetFileTime** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato nell'elenco seguente.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

Il formato di *strFileTime* non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Al termine di una chiamata a **SetFileTime**, il valore [**DateTime**](datetime.md) viene sempre interpretato come valore assoluto (**DateTime**) e l' [**intervallo**](swbemdatetime-isinterval.md) è impostato su **false**.

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

[**SWbemDateTime. SetVarDate**](swbemdatetime-setvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

