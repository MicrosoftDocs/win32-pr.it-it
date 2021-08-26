---
description: Il metodo SetWaiting incrementa il numero di thread in attesa.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Metodo CBaseAllocator.SetWaiting (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 674528b6da53b7835e437afac9a0564f91785b2f9a13f132e87a6763b80881c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057461"
---
# <a name="cbaseallocatorsetwaiting-method"></a>Metodo CBaseAllocator.SetWaiting

Il `SetWaiting` metodo incrementa il numero di thread in attesa.

## <a name="syntax"></a>Sintassi


```C++
void SetWaiting();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo incrementa la variabile membro [**CBaseAllocator::m \_ lWaiting.**](cbaseallocator-m-lwaiting.md) Se un thread è bloccato nel metodo [**CBaseAllocator::GetBuffer,**](cbaseallocator-getbuffer.md) l'allocatore chiama e quindi attende che il semaforo `SetWaiting` [**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md) sia segnalato. Il [**metodo CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) segnala il semaforo e imposta *m \_ lWaiting* su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




