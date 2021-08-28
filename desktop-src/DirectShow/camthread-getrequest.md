---
description: Il metodo GetRequest attende la richiesta successiva.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Metodo CAMThread.GetRequest (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2527d43dfa59ab01bc57109bd2845e5da8286524612746067b1ff2f4cb2a3c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103201"
---
# <a name="camthreadgetrequest-method"></a>Metodo CAMThread.GetRequest

Il `GetRequest` metodo attende la richiesta successiva.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetRequest();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore definito dalla classe derivata.

## <a name="remarks"></a>Commenti

Questo metodo si blocca fino a quando un altro thread non chiama il metodo [**CAMThread::CallWorker.**](camthread-callworker.md) Restituisce quindi il parametro passato a CallWorker. Chiamare il [**metodo CAMThread::Reply**](camthread-reply.md) per rilasciare il thread richiedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




