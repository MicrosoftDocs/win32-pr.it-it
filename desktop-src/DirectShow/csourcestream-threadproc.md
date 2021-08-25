---
description: Il metodo ThreadProc è la routine del thread di lavoro. Questo metodo implementa il metodo CAMThread::ThreadProc virtuale puro.
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Metodo CSourceStream.ThreadProc (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ef0d29ab46ada118dc97c2d767b8377556086b949b6b9969cf5671b51e5359
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915271"
---
# <a name="csourcestreamthreadproc-method"></a>Metodo CSourceStream.ThreadProc

Il `ThreadProc` metodo è la routine del thread di lavoro. Questo metodo implementa il metodo [**CAMThread::ThreadProc virtuale**](camthread-threadproc.md) puro.

## <a name="syntax"></a>Sintassi


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 se il thread è stato completato correttamente o 1 in caso contrario. Se il valore restituito è 1, le risorse del thread potrebbero essere ancora allocate.

## <a name="remarks"></a>Commenti

Questo metodo attende per un tempo indefinito le richieste di thread, chiamando il [**metodo CAMThread::GetRequest.**](camthread-getrequest.md) Se riceve una richiesta [**CSourceStream::Run**](csourcestream-run.md) o [**CSourceStream::P ause,**](csourcestream-pause.md) chiama il metodo [**CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md) Il **metodo DoBufferProcessingLoop** esegue il push dei dati fino a quando non riceve una [**richiesta CSourceStream::Stop.**](csourcestream-stop.md) La routine del thread viene chiusa quando riceve una [**richiesta CSourceStream::Exit.**](csourcestream-exit.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




