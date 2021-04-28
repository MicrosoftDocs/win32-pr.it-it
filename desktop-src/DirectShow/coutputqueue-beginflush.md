---
description: "Metodo COutputQueue.BeginFlush: il metodo BeginFlush avvia un'operazione di scaricamento."
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Metodo COutputQueue.BeginFlush (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7c6168daf766ec11e18e86673d9d25542b50462
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099029"
---
# <a name="coutputqueuebeginflush-method"></a>Metodo COutputQueue.BeginFlush

Il `BeginFlush` metodo avvia un'operazione di scaricamento.

## <a name="syntax"></a>Sintassi


```C++
void BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo imposta la [**variabile membro COutputQueue::m \_ bFlushing**](coutputqueue-m-bflushing.md) su **TRUE.** Se l'oggetto usa un thread, il thread chiama il metodo [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) per liberare eventuali esempi in sospeso. In caso contrario, **l'oggetto chiama FreeSamples** durante [**il metodo COutputQueue::EndFlush.**](coutputqueue-endflush.md) Questo metodo imposta anche la variabile membro [**COutputQueue::m \_ hr**](coutputqueue-m-hr.md) su S FALSE, in modo che l'oggetto scarti \_ tutti i nuovi esempi.

L'oggetto passa la notifica di scaricamento a valle chiamando il [**metodo IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




