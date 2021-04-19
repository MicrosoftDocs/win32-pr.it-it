---
description: Il metodo ResetEndOfStreamTimer Annulla il timer che pianifica le \_ notifiche complete di EC.
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: Metodo CBaseRenderer. ResetEndOfStreamTimer (Renbase. h)
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
ms.openlocfilehash: 734673c4e2bd6719179eca00f03a6c2f41061132
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333330"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a>CBaseRenderer. ResetEndOfStreamTimer, metodo

Il `ResetEndOfStreamTimer` metodo annulla il timer che pianifica le notifiche [**\_ complete di EC**](ec-complete.md) .

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
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md)
</dt> <dt>

[**CBaseRenderer:: TimerCallback**](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




