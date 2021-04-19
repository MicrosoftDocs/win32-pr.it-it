---
description: Il metodo IsSpecialSample determina se i dati in coda sono un messaggio di controllo.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Metodo COutputQueue. IsSpecialSample (Outputq. h)
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
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325753"
---
# <a name="coutputqueueisspecialsample-method"></a>COutputQueue. IsSpecialSample, metodo

Il `IsSpecialSample` metodo determina se i dati in coda sono un messaggio di controllo.

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

Puntatore a un elemento della coda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se *pSample* è un messaggio di controllo. in caso contrario, **false** .

## <a name="remarks"></a>Commenti

Il metodo [**COutputQueue:: QueueSample**](coutputqueue-queuesample.md) può ricevere i messaggi di controllo oltre agli esempi di supporti. Un messaggio di controllo è una costante definita (di cui viene eseguito il cast a un \_ tipo Long PTR) che indica al thread di eseguire un'azione. I messaggi di controllo non contengono dati multimediali. Per ulteriori informazioni, vedere **COutputQueue:: QueueSample**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




