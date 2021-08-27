---
description: Matrice di esempi di dimensioni COutputQueue::m \_ lBatchSize.
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: Membro COutputQueue::m_ppSamples (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0b27a356727fc317eb1818ecd548d944e3c4b2ace9cc11e0834bf1cf551c9f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103151"
---
# <a name="coutputqueuem_ppsamples-member"></a>Membro COutputQueue::m \_ ppSamples

Matrice di esempi di dimensioni [**COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).

## <a name="syntax"></a>Sintassi


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>Osservazioni

Il thread di lavoro esegue il pull degli esempi dalla coda e li inserisce in questa matrice. Passa la matrice al [**metodo IMemInputPin::ReceiveMultiple.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) Se l'oggetto non usa un thread di lavoro, l'oggetto inserisce gli esempi direttamente in questa matrice. La [**variabile membro COutputQueue::m \_ List**](coutputqueue-m-list.md) contiene la coda.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




