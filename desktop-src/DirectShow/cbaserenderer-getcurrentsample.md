---
description: Il metodo GetCurrentSample recupera l'esempio corrente.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Metodo CBaseRenderer.GetCurrentSample (Renbase.h)
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
ms.openlocfilehash: 5ffe3cdf95d5ab248956e670c04572140fa4621fff5b0cb5183f9a7cbd9b837e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822722"
---
# <a name="cbaserenderergetcurrentsample-method"></a>Metodo CBaseRenderer.GetCurrentSample

Il `GetCurrentSample` metodo recupera l'esempio corrente.

## <a name="syntax"></a>Sintassi


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'interfaccia [**IMediaSample dell'esempio**](/windows/desktop/api/Strmif/nn-strmif-imediasample) oppure **NULL** se non è disponibile alcun esempio.

## <a name="remarks"></a>Commenti

A meno che il metodo non **restituisca NULL,** il metodo chiama **AddRef** sul puntatore [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) prima di restituirlo. Il chiamante deve rilasciare il puntatore . Per implicazione, è necessario assegnare il valore restituito a una variabile, in modo da poterlo rilasciare in un secondo momento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




