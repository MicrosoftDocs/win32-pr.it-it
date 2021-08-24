---
description: Se è disponibile un evento, il metodo NextEvent dell'oggetto SWbemEventSource recupera l'evento da una query di eventi.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Metodo SWbemEventSource.NextEvent (Wbemdisp.h)
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
ms.openlocfilehash: 6ce39d442b48f32c2aafcd6e24c1c214dce82a19435b6b36bce65d5426161859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050069"
---
# <a name="swbemeventsourcenextevent-method"></a>Metodo SWbemEventSource.NextEvent

Se è disponibile un evento, il **metodo NextEvent** dell'oggetto [**SWbemEventSource**](swbemeventsource.md) recupera l'evento da una query di eventi.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

Numero di millisecondi in cui la chiamata attende un evento prima di restituire un errore di timeout. Il valore predefinito per questo parametro è **wbemTimeoutInfinite** (-1), che indica alla chiamata di attendere per un periodo illimitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il **metodo NextEvent** ha esito positivo, restituisce un [**oggetto SWbemObject**](swbemobject.md) che contiene l'evento richiesto. Se si verifica il timeout della chiamata, l'oggetto restituito **è NULL** e viene generato un errore.

## <a name="error-codes"></a>Codici di errore

Al termine del metodo **NextEvent,** **l'oggetto Err** può contenere il codice di errore nell'elenco seguente.

<dl> <dt>

**wbemErrTimedOut** - 0x80043001
</dt> <dd>

L'evento richiesto non è arrivato nel periodo di tempo specificato in *iTimeoutMs.*

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



 

 




