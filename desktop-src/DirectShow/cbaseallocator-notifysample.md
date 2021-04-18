---
description: Il metodo NotifySample rilascia tutti i thread in attesa di esempi.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Metodo CBaseAllocator. NotifySample (Amfilter. h)
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
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331805"
---
# <a name="cbaseallocatornotifysample-method"></a>CBaseAllocator. NotifySample, metodo

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

Quando sono presenti thread in attesa di campioni, il valore di [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) è maggiore di zero. Se *m \_ lWaiting* è maggiore di zero, questo metodo chiama la funzione **ReleaseSemaphore** sul semaforo [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) , attivando eventuali thread in attesa. Reimposta anche *m \_ lWaiting* su zero.

Questo metodo viene chiamato dall'interno del metodo [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) , quando un campione viene restituito all'elenco di disponibilità. e dal metodo [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , quando viene eseguito il commit dell'allocatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




