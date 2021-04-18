---
description: Puntatore a una sezione critica utilizzata per serializzare le modifiche di stato.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Membro CBaseFilter:: m_pLock (Amfilter. h)'
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
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327219"
---
# <a name="cbasefilterm_plock-member"></a>Membro pLock di CBaseFilter:: m \_

Puntatore a una sezione critica utilizzata per serializzare le modifiche di stato.

## <a name="syntax"></a>Sintassi


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Osservazioni

Questa variabile viene inizializzata nel costruttore della classe; vedere [**CBaseFilter:: CBaseFilter**](cbasefilter-cbasefilter.md).

Questa sezione critica viene mantenuta durante le transizioni di stato o quando un metodo accede allo stato su più operazioni. La classe base include la sezione Critical nei metodi seguenti:

-   [**CBaseFilter::FindPin**](cbasefilter-findpin.md)
-   [**CBaseFilter::GetSyncSource**](cbasefilter-getsyncsource.md)
-   [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md)
-   [**CBaseFilter:: inattivo**](cbasefilter-isactive.md)
-   [**CBaseFilter::SetSyncSource**](cbasefilter-setsyncsource.md)
-   [**CBaseFilter::P ause**](cbasefilter-pause.md)
-   [**CBaseFilter:: Run**](cbasefilter-run.md)
-   [**CBaseFilter:: Stop**](cbasefilter-stop.md)

Non mantenere questa sezione critica durante le operazioni di streaming, ovvero durante la distribuzione di campioni a un filtro downstream. Serializzare le operazioni di streaming usando un'altra sezione critica. In caso contrario, può causare un deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> <dt>

[Thread e sezioni critiche](threads-and-critical-sections.md)
</dt> </dl>

 

 




