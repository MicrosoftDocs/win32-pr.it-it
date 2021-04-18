---
description: Il metodo GetRequest attende la richiesta successiva.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Metodo CAMThread. GetRequest (Wxutil. h)
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
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329878"
---
# <a name="camthreadgetrequest-method"></a>Metodo CAMThread. GetRequest

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

Questo metodo si blocca fino a quando un altro thread chiama il metodo [**CAMThread:: CallWorker**](camthread-callworker.md) . Restituisce quindi il parametro passato a CallWorker. Chiamare il metodo [**CAMThread:: Reply**](camthread-reply.md) per rilasciare il thread richiedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




