---
description: Metodo del distruttore.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: Distruttore CAMThread. ~ CAMThread (Wxutil. h)
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
ms.openlocfilehash: b0b0a4dde858811a75347105b9fccd2f499c4faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329164"
---
# <a name="camthreadcamthread-destructor"></a>Distruttore CAMThread. ~ CAMThread

Metodo del distruttore.

## <a name="syntax"></a>Sintassi


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Osservazioni

Il distruttore chiama il metodo [**CAMThread:: Close**](camthread-close.md) , che attende la chiusura del thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




