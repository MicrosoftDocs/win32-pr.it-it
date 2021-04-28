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
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095409"
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
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




