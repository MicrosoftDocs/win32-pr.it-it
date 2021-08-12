---
description: Numero di buffer da fornire.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: Membro CBaseAllocator::m_lCount (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c33749ee6293c301501962939e25118595db10592713fb46dc10d01083c0096f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661693"
---
# <a name="cbaseallocatorm_lcount-member"></a>Membro CBaseAllocator::m \_ lCount

Numero di buffer da fornire. Il [**metodo CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) imposta questo valore. I buffer non vengono allocati fino a quando non viene chiamato il metodo [**CBaseAllocator::Commit.**](cbaseallocator-commit.md) Il numero corrente di buffer allocati viene specificato dalla variabile membro [**CBaseAllocator::m \_ lAllocated.**](cbaseallocator-m-lallocated.md)

## <a name="syntax"></a>Sintassi


```C++
long m_lCount;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




