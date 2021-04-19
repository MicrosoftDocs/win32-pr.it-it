---
description: Il metodo TimerCallback è un metodo di callback per l'evento timer di fine flusso.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Metodo CBaseRenderer. TimerCallback (Renbase. h)
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
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332989"
---
# <a name="cbaserenderertimercallback-method"></a>CBaseRenderer. TimerCallback, metodo

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

Il metodo [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) usa un evento timer per pianificare le \_ notifiche complete di EC. Il metodo **CBaseRenderer:: TimerCallback** è la funzione di callback per l'evento del timer. Il `TimerCallback` metodo chiama di nuovo **SendEndOfStream** e **SendEndOfStream** determina se inviare la notifica di \_ completamento EC o impostare un altro timer.

Il metodo [**CBaseRenderer:: ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) Annulla l'evento del timer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




