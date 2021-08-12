---
description: Il metodo CheckRequest verifica se è presente una richiesta, senza bloccarsi.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Metodo CAMThread.CheckRequest (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 292f8a7fb1ed4f12ad558993d6b1932b2ddff4656bada5e0a89067bac1baa9c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662357"
---
# <a name="camthreadcheckrequest-method"></a>Metodo CAMThread.CheckRequest

Il `CheckRequest` metodo verifica se è presente una richiesta, senza bloccarsi.

## <a name="syntax"></a>Sintassi


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pParam* 
</dt> <dd>

Puntatore a una variabile che riceve il valore passato nell'ultima chiamata al [**metodo CAMThread::CallWorker.**](camthread-callworker.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** è presente una richiesta in sospeso oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Questo metodo è una versione non bloccante del [**metodo CAMThread::GetRequest.**](camthread-getrequest.md)

Se un altro thread è in attesa di una chiamata a CallWorker, questo metodo recupera il parametro della richiesta e restituisce **TRUE.** In caso contrario, restituisce **FALSE.** Se il metodo restituisce **TRUE,** chiamare il [**metodo CAMThread::Reply**](camthread-reply.md) per rilasciare il thread richiedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




