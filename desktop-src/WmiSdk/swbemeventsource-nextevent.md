---
description: Se è disponibile un evento, il metodo NextEvent dell'oggetto SWbemEventSource recupera l'evento da una query di eventi.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Metodo SWbemEventSource. NextEvent (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318516"
---
# <a name="swbemeventsourcenextevent-method"></a>SWbemEventSource. NextEvent, metodo

Se è disponibile un evento, il metodo **NextEvent** dell'oggetto [**SWbemEventSource**](swbemeventsource.md) recupera l'evento da una query di eventi.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iTimeoutMs* \[ in, facoltativo\]
</dt> <dd>

Numero di millisecondi di attesa della chiamata per un evento prima che venga restituito un errore di timeout. Il valore predefinito per questo parametro è **wbemTimeoutInfinite** (-1), che indirizza la chiamata a un'attesa indefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo **NextEvent** ha esito positivo, restituisce un oggetto [**SWbemObject**](swbemobject.md) che contiene l'evento richiesto. Se si verifica il timeout della chiamata, l'oggetto restituito è **null** e viene generato un errore.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **NextEvent** , l'oggetto **Err** può contenere il codice di errore riportato nell'elenco seguente.

<dl> <dt>

**wbemErrTimedOut** -0x80043001
</dt> <dd>

L'evento richiesto non è arrivato nell'intervallo di tempo specificato in *iTimeoutMs.*

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMEVENTSOURCE CLSID<br/>                                                      |
| IID<br/>                      | \_ISWBEMEVENTSOURCE IID<br/>                                                       |



 

 




