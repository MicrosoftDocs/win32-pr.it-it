---
description: Il metodo GetFilterGraph recupera un puntatore al gestore del grafico del filtro.
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: Metodo CBaseFilter.GetFilterGraph (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f35b40febff058d5bbd9f48c5ac6d10168d48d6e587b51ab2730704724e48c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056651"
---
# <a name="cbasefiltergetfiltergraph-method"></a>Metodo CBaseFilter.GetFilterGraph

Il `GetFilterGraph` metodo recupera un puntatore al gestore del grafico del filtro.

## <a name="syntax"></a>Sintassi


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore di [**CBaseFilter::m \_ pGraph**](cbasefilter-m-pgraph.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




