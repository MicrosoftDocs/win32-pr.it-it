---
description: Converte una data nel formato stringa FILETIME nel formato cim datetime.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Metodo SWbemDateTime.SetFileTime (Wbemdisp.h)
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
ms.openlocfilehash: 138685ba4d6b63591bf460da3cdba219685f015d54789ca60a52660845b2e41a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739458"
---
# <a name="swbemdatetimesetfiletime-method"></a>Metodo SWbemDateTime.SetFileTime

Il **metodo SetFileTime** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte una data nel formato **stringa FILETIME** nel formato [cim datetime.](date-and-time-format.md)

Il **formato FILETIME** è una struttura datetime a 64 bit che rappresenta il numero di unità da 100 nanosecondi dall'inizio del 1° gennaio 1601. Windows Strumentazione gestione (WMI) considera i **valori FILETIME** come rappresentazioni di stringa di numeri a 64 bit senza segno.

Per la spiegazione della sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strFileTime* \[ Pollici\]
</dt> <dd>

**Valore FILETIME** utilizzato per impostare l'oggetto.

</dd> <dt>

*bIsLocal* \[ in, facoltativo\]
</dt> <dd>

Se **TRUE,** *strFileTime viene* interpretato come ora locale. La Coordinated Universal Time (UTC) contiene l'ora locale convertita nell'offset UTC corretto. Quando *bIsLocal* è **FALSE,** *strFileTime* viene convertito direttamente in un valore UTC con offset pari a 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo aver completato il **metodo SetFileTime,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore nell'elenco seguente.

<dl> <dt>

**wbemErrInvalidSyntax** - 2147749921 (0x80041021)
</dt> <dd>

Il formato di *strFileTime* non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Dopo una chiamata riuscita a **SetFileTime**, il valore [**datetime**](datetime.md) viene sempre interpretato come valore assoluto (**datetime**) e [**IsInterval**](swbemdatetime-isinterval.md) è impostato su **FALSE**.

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

[**SWbemDateTime.SetVarDate**](swbemdatetime-setvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

