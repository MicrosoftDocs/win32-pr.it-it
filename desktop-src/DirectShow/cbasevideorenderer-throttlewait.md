---
description: Il metodo ThrottleWait inserisce un periodo di attesa dopo ogni frame.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: Metodo CBaseVideoRenderer.ThrottleWait (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d61c0e934208ad72e678595ce668c6c7ff72eda3371c792b294df9f2d5915612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954750"
---
# <a name="cbasevideorendererthrottlewait-method"></a>Metodo CBaseVideoRenderer.ThrottleWait

Il `ThrottleWait` metodo inserisce un periodo di attesa dopo ogni frame.

## <a name="syntax"></a>Sintassi


```C++
void ThrottleWait();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro attende un periodo di tempo ottenuto dal membro **\_ dati m trThrottle.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




