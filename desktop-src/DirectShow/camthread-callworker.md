---
description: Il metodo CallWorker segnala al thread una richiesta.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Metodo CAMThread.CallWorker (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7ffee6a55191f8f41d7121f3801a4a6392f9869803ded40ed891817146828f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955400"
---
# <a name="camthreadcallworker-method"></a>Metodo CAMThread.CallWorker

Il `CallWorker` metodo segnala al thread una richiesta.

## <a name="syntax"></a>Sintassi


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwParam* 
</dt> <dd>

Parametro della richiesta. La classe derivata definisce il significato del parametro .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore definito dalla classe derivata.

## <a name="remarks"></a>Commenti

I [**metodi CAMThread::GetRequest**](camthread-getrequest.md) e [**CAMThread::CheckRequest**](camthread-checkrequest.md) recuperano il valore del *parametro dwParam.* Il metodo GetRequest si blocca fino a quando `CallWorker` non viene chiamato .

Questo metodo si blocca fino a quando non viene chiamato il metodo [**CAMThread::Reply.**](camthread-reply.md) Il valore restituito è il parametro assegnato a Reply.

Questo metodo contiene il [**blocco \_ ACCESSLock CAMThread::m**](camthread-m-accesslock.md) per serializzare le richieste. Pertanto, chiamare questo metodo dal thread stesso o da qualsiasi funzione membro eseguita nel contesto del thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




