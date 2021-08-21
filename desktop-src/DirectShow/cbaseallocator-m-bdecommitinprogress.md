---
description: Flag che indica se è in corso un'operazione di decommit.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: Membro CBaseAllocator::m_bDecommitInProgress (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6d73514ffbe2b6e2430230e64ccfa9006809523a95cd3220ca078d4c4e40f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017539"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>Membro CBaseAllocator::m \_ bDecommitInProgress

Flag che indica se è in corso un'operazione di decommit. Il valore **è TRUE** dopo la chiamata del metodo [**CBaseAllocator::D ecommit,**](cbaseallocator-decommit.md) ma prima del rilascio di tutti i buffer. Se il valore è **TRUE,** il [**metodo CBaseAllocator::GetBuffer ha**](cbaseallocator-getbuffer.md) esito negativo. Inoltre, l'allocatore non deve eliminare se stesso mentre il valore è **TRUE.**

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




