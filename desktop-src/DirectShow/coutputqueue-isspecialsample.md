---
description: Il metodo IsSpecialSample determina se i dati in coda sono messaggi di controllo.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Metodo COutputQueue.IsSpecialSample (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c192196869f86e8d78da2f6b38a661373e115753d99e554f4b7a868eb0b484fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688221"
---
# <a name="coutputqueueisspecialsample-method"></a>Metodo COutputQueue.IsSpecialSample

Il `IsSpecialSample` metodo determina se i dati in coda sono messaggi di controllo.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore a un elemento nella coda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** *pSample è* un messaggio di controllo oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Il [**metodo COutputQueue::QueueSample**](coutputqueue-queuesample.md) può ricevere messaggi di controllo oltre agli esempi multimediali. Un messaggio di controllo è una costante definita (cast a un tipo LONG PTR) che indica al \_ thread di eseguire un'azione. I messaggi di controllo non contengono dati multimediali. Per altre informazioni, vedere **COutputQueue::QueueSample**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




