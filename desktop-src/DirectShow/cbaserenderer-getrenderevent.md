---
description: Il metodo GetRenderEvent recupera l'evento che pianifica il rendering.
ms.assetid: da0272f6-6a1d-4c07-a907-822227b56305
title: Metodo CBaseRenderer.GetRenderEvent (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRenderEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04b4adc030e172a3d66d501e745ca9e3d1062fc1551bccb504fff36328d00bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822658"
---
# <a name="cbaserenderergetrenderevent-method"></a>Metodo CBaseRenderer.GetRenderEvent

Il `GetRenderEvent` metodo recupera l'evento che pianifica il rendering.

## <a name="syntax"></a>Sintassi


```C++
CAMEvent* GetRenderEvent();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore [**all'evento \_ RenderEvent CBaseRenderer::m.**](cbaserenderer-m-renderevent.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




