---
description: Il metodo NotifySample rilascia tutti i thread in attesa di esempi.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Metodo CBaseAllocator.NotifySample (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b1b73a54ae9b5ccabacfbb1153c5d0d91f951e83082a1bdd3c7f7551ad813804
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017479"
---
# <a name="cbaseallocatornotifysample-method"></a>Metodo CBaseAllocator.NotifySample

Il `NotifySample` metodo rilascia tutti i thread in attesa di esempi.

## <a name="syntax"></a>Sintassi


```C++
void NotifySample();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando sono presenti thread in attesa di esempi, il valore di [**CBaseAllocator::m \_ lWaiting**](cbaseallocator-m-lwaiting.md) è maggiore di zero. Se *m \_ lWaiting* è maggiore di zero, questo metodo chiama la funzione **ReleaseSemaphore** sul semaforo [**CBaseAllocator::m \_ hSem,**](cbaseallocator-m-hsem.md) attivando tutti i thread in attesa. Reimposta anche *m \_ lWaiting* su zero.

Questo metodo viene chiamato dall'interno del [**metodo CBaseAllocator::ReleaseBuffer,**](cbaseallocator-releasebuffer.md) quando un esempio viene restituito all'elenco gratuito; e dal metodo [**CBaseAllocator::D ecommit,**](cbaseallocator-decommit.md) quando viene eseguito il decommit dell'allocatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




