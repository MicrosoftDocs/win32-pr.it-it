---
description: Distruttore CAMThread.~CAMThread - Metodo distruttore.
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
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096439"
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
| Intestazione<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




