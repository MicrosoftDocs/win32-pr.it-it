---
description: Il metodo GetRequestHandle recupera un handle per l'evento segnalato dal metodo CAMThread::CallWorker.
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Metodo CAMThread.GetRequestHandle (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fa1be333ff35821f187cea980746c6b729a05c12e2103f4465bb44bbcc6f9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652591"
---
# <a name="camthreadgetrequesthandle-method"></a>Metodo CAMThread.GetRequestHandle

Il `GetRequestHandle` metodo recupera un handle per l'evento segnalato dal metodo [**CAMThread::CallWorker.**](camthread-callworker.md)

## <a name="syntax"></a>Sintassi


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un handle di evento.

## <a name="remarks"></a>Commenti

La classe CAMEvent mantiene un evento di reimpostazione manuale privato, impostato da CallWorker e reimpostato dal [**metodo CAMThread::Reply.**](camthread-reply.md)

Se si chiama una funzione come WaitForMultipleObjects, usare GetRequestHandle per recuperare l'handle dell'evento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




