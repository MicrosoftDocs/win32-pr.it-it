---
description: Metodo del distruttore.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: Distruttore CBaseAllocator. ~ CBaseAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324043"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>Distruttore CBaseAllocator. ~ CBaseAllocator

Metodo del distruttore.

## <a name="syntax"></a>Sintassi


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Osservazioni

Chiamare sempre il metodo [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) prima di eliminare l'oggetto. Il distruttore della classe base non può chiamare il metodo **decommit**, perché il metodo chiama il metodo virtuale pure [**CBaseAllocator:: Free**](cbaseallocator-free.md). Le classi derivate devono eseguire l'override di questo distruttore e chiamare **decommit**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




