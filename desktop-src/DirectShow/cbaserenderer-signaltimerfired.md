---
description: Il metodo SignalTimerFired cancella l'identificatore del timer usato per pianificare il rendering.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Metodo CBaseRenderer.SignalTimerFired (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f08ed0e8348648d5d1af1127159b414b0ddbc40cfd470ff0834b7bc2b0723e9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052361"
---
# <a name="cbaserenderersignaltimerfired-method"></a>Metodo CBaseRenderer.SignalTimerFired

Il `SignalTimerFired` metodo cancella l'identificatore del timer usato per pianificare il rendering.

## <a name="syntax"></a>Sintassi


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il filtro chiama questo metodo quando viene attivato il timer di rendering (vedere [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) o quando il timer viene annullato (vedere [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)). Il metodo reimposta la variabile membro [**CBaseRenderer::m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




