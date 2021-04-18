---
description: 'Il metodo ThreadProc è la procedura del thread per il thread di lavoro. Questo metodo implementa il metodo CAMThread:: ThreadProc virtuale puro.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Metodo CSourceStream. ThreadProc (source. h)
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
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325658"
---
# <a name="csourcestreamthreadproc-method"></a>CSourceStream. ThreadProc, metodo

Il `ThreadProc` metodo è la procedura del thread per il thread di lavoro. Questo metodo implementa il metodo [**CAMThread:: ThreadProc**](camthread-threadproc.md) virtuale puro.

## <a name="syntax"></a>Sintassi


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 se il thread è stato completato correttamente o 1 in caso contrario. Se il valore restituito è 1, le risorse del thread potrebbero ancora essere allocate.

## <a name="remarks"></a>Commenti

Questo metodo attende a tempo indefinito per le richieste di thread, chiamando il metodo [**CAMThread:: GetRequest**](camthread-getrequest.md) . Se riceve una richiesta [**CSourceStream:: Run**](csourcestream-run.md) o [**CSourceStream::P ause**](csourcestream-pause.md) , chiama il metodo [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . Il metodo **DoBufferProcessingLoop** esegue il push dei dati fino a quando non riceve una richiesta [**CSourceStream:: Stop**](csourcestream-stop.md) . La procedura del thread viene chiusa quando riceve una richiesta [**CSourceStream:: Exit**](csourcestream-exit.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




