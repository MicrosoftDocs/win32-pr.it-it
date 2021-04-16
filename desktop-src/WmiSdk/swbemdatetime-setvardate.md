---
description: Converte una data nel \_ formato di data VT nel formato DateTime CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Metodo SWbemDateTime. SetVarDate (wbemdisp. h)
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
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348886"
---
# <a name="swbemdatetimesetvardate-method"></a>SWbemDateTime. SetVarDate, metodo

Il metodo **SetVarDate** dell'oggetto [**SWbemDateTime**](swbemdatetime.md) converte una data nel formato di **\_ Data VT** nel formato [DateTime CIM](date-and-time-format.md) .

Un valore di **\_ Data VT** è un valore datetime Variant che Visual Basic e ActiveX usano.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Vdate* \[ in\]
</dt> <dd>

Valore della data Variant per l'impostazione dell'oggetto. Questo parametro deve essere nel formato **di \_ Data VT** .

</dd> <dt>

*bIsLocal* \[ in, facoltativo\]
</dt> <dd>

Se è **true**, *Vdate* viene interpretato come ora locale e la proprietà UTC (Coordinated Universal Time) contiene l'ora locale convertita nell'offset UTC corretto. Quando *bIsLocal* è **false**, *Vdate* viene convertito direttamente in un valore UTC con un offset pari a zero (0).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo aver completato il metodo **SetVarDate** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere il codice di errore riportato nell'elenco seguente.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

Il formato di *Vdate* non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Dopo una chiamata a **SetVarDate**, il valore [**DateTime**](datetime.md) viene interpretato come valore DateTime assoluto anziché come intervallo e la proprietà di [**intervallo**](swbemdatetime-isinterval.md) è impostata su **false**.

La funzione intrinseca Visual Basic o VBScript [CDate](/previous-versions//2dt118h2(v=vs.85)) fornisce un valore [**DateTime**](datetime.md) nel formato di **\_ Data VT** per l'input in **SetVarDate**.

## <a name="examples"></a>Esempio

Per esempi relativi all'uso dell'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertire valori [**DateTime**](datetime.md) CIM in e dal formato **FILETIME** o dal formato **\_ Data VT** , vedere [attività WMI: date e ore](wmi-tasks--dates-and-times.md). Per una descrizione del formato **DateTime** CIM, vedere [formato di data e ora](date-and-time-format.md).

L'esempio di codice [Convert date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript della raccolta TechNet USA SetVarDate per convertire un valore di data e ora normale nel formato di data e ora UTC.

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

[**SWbemDateTime. SetFileTime**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

