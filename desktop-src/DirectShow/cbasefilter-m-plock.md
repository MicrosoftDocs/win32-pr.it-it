---
description: Puntatore a una sezione critica utilizzata per serializzare le modifiche dello stato.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: Membro CBaseFilter::m_pLock (Amfilter.h)
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
ms.openlocfilehash: 3bc8d3b627e6cd8c3ae4821864f6980db5acd251c721bb8841be40e04377ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659794"
---
# <a name="cbasefilterm_plock-member"></a>Membro CBaseFilter::m \_ pLock

Puntatore a una sezione critica utilizzata per serializzare le modifiche dello stato.

## <a name="syntax"></a>Sintassi


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Osservazioni

Questa variabile viene inizializzata nel costruttore della classe. vedere [**CBaseFilter::CBaseFilter**](cbasefilter-cbasefilter.md).

Mantenere questa sezione critica durante le transizioni di stato o quando un metodo accede allo stato su più operazioni. La classe base contiene la sezione critica nei metodi seguenti:

-   [**CBaseFilter::FindPin**](cbasefilter-findpin.md)
-   [**CBaseFilter::GetSyncSource**](cbasefilter-getsyncsource.md)
-   [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md)
-   [**CBaseFilter::IsActive**](cbasefilter-isactive.md)
-   [**CBaseFilter::SetSyncSource**](cbasefilter-setsyncsource.md)
-   [**CBaseFilter::P ause**](cbasefilter-pause.md)
-   [**CBaseFilter::Run**](cbasefilter-run.md)
-   [**CBaseFilter::Stop**](cbasefilter-stop.md)

Non mantenere questa sezione critica durante le operazioni di streaming, ovvero quando si forniscono esempi a un filtro downstream. Serializzare le operazioni di streaming usando una sezione critica diversa. In caso contrario, può causare un deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> <dt>

[Thread e sezioni critiche](threads-and-critical-sections.md)
</dt> </dl>

 

 




