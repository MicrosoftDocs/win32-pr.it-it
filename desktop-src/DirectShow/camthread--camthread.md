---
description: 'Distruttore CAMThread.~CAMThread : metodo del distruttore.'
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: Distruttore CAMThread.~CAMThread (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 884460b0c1af3b96a610a18b7475d2a144dc32bf308ea0e0191f0f526565726a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662377"
---
# <a name="camthreadcamthread-destructor"></a>Distruttore CAMThread.~CAMThread

Metodo del distruttore.

## <a name="syntax"></a>Sintassi


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Osservazioni

Il distruttore chiama il [**metodo CAMThread::Close,**](camthread-close.md) che attende la chiusura del thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




