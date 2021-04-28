---
description: "Metodo COutputQueue.EndFlush: il metodo EndFlush termina un'operazione di scaricamento."
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Metodo COutputQueue.EndFlush (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37701526de66c8cd679f6849703c4eb2a1feb3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099009"
---
# <a name="coutputqueueendflush-method"></a>Metodo COutputQueue.EndFlush

Il `EndFlush` metodo termina un'operazione di scaricamento.

## <a name="syntax"></a>Sintassi


```C++
void EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se l'oggetto usa un thread, questo metodo attende l'evento [**COutputQueue::m \_ evFlushComplete.**](coutputqueue-m-evflushcomplete.md) Il thread segnala questo evento dopo aver liberato eventuali campioni in sospeso. Se l'oggetto non usa un thread, questo metodo chiama il [**metodo COutputQueue::FreeSamples.**](coutputqueue-freesamples.md) Il metodo `EndFlush` chiama quindi il metodo [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




