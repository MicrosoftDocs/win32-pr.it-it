---
description: Il metodo GetCurrentSample recupera l'esempio corrente.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Metodo CBaseRenderer. GetCurrentSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329381"
---
# <a name="cbaserenderergetcurrentsample-method"></a>CBaseRenderer. GetCurrentSample, metodo

Il `GetCurrentSample` metodo recupera l'esempio corrente.

## <a name="syntax"></a>Sintassi


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio oppure **null** se non è disponibile alcun campione.

## <a name="remarks"></a>Commenti

A meno che il metodo non restituisca **null**, il metodo chiama **AddRef** sul puntatore [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) prima di restituirlo. Il chiamante deve rilasciare il puntatore. In modo implicito, è necessario assegnare il valore restituito a una variabile, in modo che sia possibile rilasciarlo in un secondo momento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




