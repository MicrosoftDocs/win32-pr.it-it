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
ms.openlocfilehash: d9a283867036254b7a13b45ba152c3f16ecccbdb59d4d59e98c8d1dae7480e13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634221"
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

Se l'oggetto usa un thread, questo metodo attende [**l'evento COutputQueue::m \_ evFlushComplete.**](coutputqueue-m-evflushcomplete.md) Il thread segnala questo evento dopo aver liberato eventuali esempi in sospeso. Se l'oggetto non usa un thread, questo metodo chiama il metodo [**COutputQueue::FreeSamples.**](coutputqueue-freesamples.md) Il metodo `EndFlush` chiama quindi il metodo [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




