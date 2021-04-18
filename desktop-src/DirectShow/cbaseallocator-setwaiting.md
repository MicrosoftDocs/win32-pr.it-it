---
description: Il metodo di attesa incrementa il numero di thread in attesa.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Metodo CBaseAllocator. sewaiting (Amfilter. h)
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
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331797"
---
# <a name="cbaseallocatorsetwaiting-method"></a>Metodo CBaseAllocator. sewaiting

Il `SetWaiting` metodo incrementa il conteggio dei thread in attesa.

## <a name="syntax"></a>Sintassi


```C++
void SetWaiting();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo incrementa la variabile membro [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) . Se un thread è bloccato nel metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) , l'allocatore chiama `SetWaiting` e quindi attende la segnalazione del semaforo [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) . Il metodo [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) segnala il semaforo e imposta *m \_ lWaiting* di nuovo su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




