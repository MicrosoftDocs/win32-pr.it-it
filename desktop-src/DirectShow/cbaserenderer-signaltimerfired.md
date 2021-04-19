---
description: Il metodo SignalTimerFired cancella l'identificatore del timer utilizzato per pianificare il rendering.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Metodo CBaseRenderer. SignalTimerFired (Renbase. h)
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
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332998"
---
# <a name="cbaserenderersignaltimerfired-method"></a>CBaseRenderer. SignalTimerFired, metodo

Il `SignalTimerFired` metodo cancella l'identificatore del timer utilizzato per pianificare il rendering.

## <a name="syntax"></a>Sintassi


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il filtro chiama questo metodo quando il timer di rendering viene attivato (vedere [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) o quando il timer viene annullato (vedere [**CBaseRenderer:: CancelNotification**](cbaserenderer-cancelnotification.md)). Il metodo reimposta la variabile membro [**CBaseRenderer:: m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




