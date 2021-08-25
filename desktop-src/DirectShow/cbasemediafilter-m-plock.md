---
description: Puntatore a una sezione critica.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: Membro CBaseMediaFilter::m_pLock (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad92cf07cc096c50ffa50f862c26f6133fc8dbb9b9b059419bb516e07cbd5daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910791"
---
# <a name="cbasemediafilterm_plock-member"></a>Membro PLock CBaseMediaFilter::m \_

Puntatore a una sezione critica.

## <a name="syntax"></a>Sintassi


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Osservazioni

La sezione critica viene mantenuta durante le transizioni di stato ([**CBaseMediaFilter::Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), quando si accede al clock di riferimento ([**CBaseMediaFilter::SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)) e nel [**metodo CBaseMediaFilter::IsActive.**](cbasemediafilter-isactive.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




