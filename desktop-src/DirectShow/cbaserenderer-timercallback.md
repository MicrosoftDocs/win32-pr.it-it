---
description: Il metodo TimerCallback è un metodo di callback per l'evento timer di fine flusso.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Metodo CBaseRenderer.TimerCallback (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d3164959ecaa701397b5550c43449884208df1110300b6a042879ac4f146584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537431"
---
# <a name="cbaserenderertimercallback-method"></a>Metodo CBaseRenderer.TimerCallback

Il `TimerCallback` metodo è un metodo di callback per l'evento timer di fine flusso.

## <a name="syntax"></a>Sintassi


```C++
void TimerCallback();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il [**metodo CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) usa un evento timer per pianificare le notifiche EC \_ COMPLETE. Il **metodo CBaseRenderer::TimerCallback** è la funzione di callback per l'evento timer. Il `TimerCallback` metodo chiama nuovamente **SendEndOfStream** e **SendEndOfStream** determina se inviare la notifica EC COMPLETE o \_ impostare un altro timer.

Il [**metodo CBaseRenderer::ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) annulla l'evento timer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




