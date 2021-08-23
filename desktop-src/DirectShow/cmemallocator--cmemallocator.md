---
description: Distruttore CMemAllocator.~CMemAllocator - Metodo del distruttore.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: Distruttore CMemAllocator.~CMemAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588b370fc56f6af547ead19c7a52758a3851dd7e46d88b90f8f621ed6002d6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954380"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>Distruttore CMemAllocator.~CMemAllocator

Metodo del distruttore.

## <a name="syntax"></a>Sintassi


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Osservazioni

Questo metodo esegue l'override del distruttore della classe base per chiamare [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) e [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




