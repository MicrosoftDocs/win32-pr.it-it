---
description: Il metodo WaitMsg attende che l'evento sia segnalato, durante l'invio dei messaggi inviati.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Metodo CAMMsgEvent.WaitMsg (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94a2169d9938a8c2ff8a1961eee0895fefd7cc8a2dd487a4193d8053d27d98ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955450"
---
# <a name="cammsgeventwaitmsg-method"></a>Metodo CAMMsgEvent.WaitMsg

Il `WaitMsg` metodo attende che l'evento sia segnalato, durante l'invio dei messaggi inviati.

## <a name="syntax"></a>Sintassi


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwTimeOut* 
</dt> <dd>

Valore di timeout facoltativo, espresso in millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se l'evento è segnalato o **FALSE se** si è verificato il timeout.

## <a name="remarks"></a>Commenti

Questo metodo chiama la funzione PeekMessage per elaborare i messaggi. Chiamare questo metodo anziché [**CAMEvent::Wait**](camevent-wait.md) se il thread deve elaborare i messaggi durante l'attesa di un evento. Se il thread non elabora i messaggi e un altro thread invia un messaggio, potrebbe verificarsi un deadlock.

Si supponga, ad esempio, di creare un thread e quindi di bloccarsi fino all'inizializzazione del thread. Se il thread invia un messaggio alla finestra chiamando la funzione SendMessage, si verifica un deadlock. Ciò è dovuto al fatto che SendMessage non restituisce finché il messaggio non è stato elaborato. La chiamata di WaitMsg consente la restituzione della chiamata SendMessage, impedendo il deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMMsgEvent**](cammsgevent.md)
</dt> </dl>

 

 




