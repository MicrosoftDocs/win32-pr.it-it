---
description: 'Distruttore CBaseAllocator.~CBaseAllocator : metodo del distruttore.'
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: Distruttore CBaseAllocator.~CBaseAllocator (Amfilter.h)
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
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096419"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>Distruttore CBaseAllocator.~CBaseAllocator

Metodo del distruttore.

## <a name="syntax"></a>Sintassi


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Osservazioni

Chiamare sempre il [**metodo CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) prima di eliminare l'oggetto. Il distruttore della classe base non può chiamare **Decommit** perché tale metodo chiama il metodo virtuale [**puro CBaseAllocator::Free.**](cbaseallocator-free.md) Le classi derivate devono eseguire l'override di questo distruttore e **chiamare Decommit**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




