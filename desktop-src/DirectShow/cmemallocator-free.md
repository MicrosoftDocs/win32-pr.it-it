---
description: Il metodo Free viene chiamato durante un'operazione di decommit.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Metodo CMemAllocator.Free (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c2ffea6fdd60e4053f6c00ee1c87ca9596560909864c861d46b5728dad13a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155993"
---
# <a name="cmemallocatorfree-method"></a>Metodo CMemAllocator.Free

Il `Free` metodo viene chiamato durante un'operazione di decommit. Questo metodo implementa il metodo [**CBaseAllocator::Free**](cbaseallocator-free.md) virtuale puro, ma non esegue alcuna operazione. La memoria del buffer non viene effettivamente rilasciata fino a **quando l'oggetto CMemAllocator** non viene eliminato. Il metodo del distruttore chiama [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md) per rilasciare la memoria.

## <a name="syntax"></a>Sintassi


```C++
void Free();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




