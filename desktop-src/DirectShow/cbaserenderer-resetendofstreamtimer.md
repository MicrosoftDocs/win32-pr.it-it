---
description: Il metodo ResetEndOfStreamTimer annulla il timer che pianifica le notifiche EC \_ COMPLETE.
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: Metodo CBaseRenderer.ResetEndOfStreamTimer (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e589288059eabbbbaaa23904ba021199cb051d9034345cb2c92ac946a6cba9c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502681"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a>Metodo CBaseRenderer.ResetEndOfStreamTimer

Il `ResetEndOfStreamTimer` metodo annulla il timer che pianifica le notifiche EC [**\_ COMPLETE.**](ec-complete.md)

## <a name="syntax"></a>Sintassi


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md)
</dt> <dt>

[**CBaseRenderer::TimerCallback**](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




