---
description: Metodo del distruttore.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: Distruttore CMemAllocator. ~ CMemAllocator (Amfilter. h)
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
ms.openlocfilehash: d49046eccd8d7ef71c4eeb4c75acffbf90f7d826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327448"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>Distruttore CMemAllocator. ~ CMemAllocator

Metodo del distruttore.

## <a name="syntax"></a>Sintassi


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Osservazioni

Questo metodo esegue l'override del distruttore della classe base per chiamare [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) e [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




