---
description: Converte una data nel formato VT \_ DATE nel formato cim datetime.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Metodo SWbemDateTime.SetVarDate (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 56d193bd2faffd51507ec4a913c7ee068b055dcf45ca756e801431659768c47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050099"
---
# <a name="swbemdatetimesetvardate-method"></a>Metodo SWbemDateTime.SetVarDate

Il **metodo SetVarDate** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte una data nel formato **VT \_ DATE** nel formato [cim datetime.](date-and-time-format.md)

Un **valore DATE \_ VT** è un valore datetime variant che Visual Basic e ActiveX usare.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vdate* \[ Pollici\]
</dt> <dd>

Valore della data della variante per impostare l'oggetto . Questo parametro deve essere nel **formato VT \_ DATE.**

</dd> <dt>

*bIsLocal* \[ in, facoltativo\]
</dt> <dd>

Se **TRUE,** *vdate* viene interpretato come ora locale e la proprietà Coordinated Universal Time (UTC) contiene l'ora locale convertita nell'offset UTC corretto. Quando *bIsLocal* è **FALSE,** *vdate* viene convertito direttamente in un valore UTC con offset pari a zero (0).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo aver completato il **metodo SetVarDate,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore nell'elenco seguente.

<dl> <dt>

**wbemErrInvalidSyntax** - 2147749921 (0x80041021)
</dt> <dd>

Il formato *di vdate* non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Dopo una chiamata a **SetVarDate** riuscita, il valore DATETIME viene interpretato come valore [**datetime**](datetime.md) assoluto anziché come intervallo e la proprietà [**IsInterval**](swbemdatetime-isinterval.md) è impostata su **FALSE.**

La funzione Visual Basic o [VBScript CDate](/previous-versions//2dt118h2(v=vs.85)) fornisce un valore [**datetime**](datetime.md) nel formato **VT \_ DATE** per l'input in **SetVarDate.**

## <a name="examples"></a>Esempio

Per esempi di utilizzo dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire i valori [**CIM DATETIME**](datetime.md) in e dal formato **FILETIME** o **VT \_ DATE,** vedere [Attività WMI:](wmi-tasks--dates-and-times.md)date e ore . Per una descrizione del formato CIM **DATETIME,** vedere [Formato di data e ora](date-and-time-format.md).

L'esempio di codice VBScript Convert [Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) in TechNet Gallery usa SetVarDate per convertire un valore di data e ora normale nel formato di data e ora UTC.

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

[**SWbemDateTime.SetFileTime**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

