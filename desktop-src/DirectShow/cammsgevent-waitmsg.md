---
description: Il metodo WaitMsg attende che l'evento venga segnalato, durante l'invio dei messaggi inviati.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Metodo CAMMsgEvent. WaitMsg (Wxutil. h)
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
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326946"
---
# <a name="cammsgeventwaitmsg-method"></a>CAMMsgEvent. WaitMsg, metodo

Il `WaitMsg` metodo attende che l'evento venga segnalato, durante l'invio dei messaggi inviati.

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

Valore di timeout facoltativo, in millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'evento viene segnalato oppure **false** se si è verificato il timeout.

## <a name="remarks"></a>Commenti

Questo metodo chiama la funzione PeekMessage per elaborare i messaggi. Chiamare questo metodo invece di [**CAMEvent:: wait**](camevent-wait.md) se il thread deve elaborare i messaggi in attesa di un evento. Se il thread non elabora i messaggi e un altro thread invia un messaggio, potrebbe verificarsi un deadlock.

Si supponga, ad esempio, di creare un thread e di bloccarlo fino a quando il thread non viene inizializzato. Se il thread invia un messaggio alla finestra chiamando la funzione SendMessage, verrà generato un deadlock. Questo perché SendMessage non restituisce un risultato fino a quando il messaggio non è stato elaborato. La chiamata a WaitMsg consente la restituzione della chiamata SendMessage, impedendo il deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMMsgEvent**](cammsgevent.md)
</dt> </dl>

 

 




