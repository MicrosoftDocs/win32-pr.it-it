---
description: Il metodo GetRenderEvent recupera l'evento che pianifica il rendering.
ms.assetid: da0272f6-6a1d-4c07-a907-822227b56305
title: Metodo CBaseRenderer. GetRenderEvent (Renbase. h)
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
ms.openlocfilehash: 9e2fd0b9cd98194129eccd2e24e6ee75577d1eec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324855"
---
# <a name="cbaserenderergetrenderevent-method"></a>CBaseRenderer. GetRenderEvent, metodo

Il `GetRenderEvent` metodo recupera l'evento che pianifica il rendering.

## <a name="syntax"></a>Sintassi


```C++
CAMEvent* GetRenderEvent();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




