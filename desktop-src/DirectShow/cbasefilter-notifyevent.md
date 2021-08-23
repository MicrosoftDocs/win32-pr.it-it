---
description: Il metodo NotifyEvent invia una notifica degli eventi al gestore del grafico del filtro.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Metodo CBaseFilter.NotifyEvent (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e21ab1275aba05331055b7a38631f8c98ae65476aacf8f17073ed1dc45c90bf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640311"
---
# <a name="cbasefilternotifyevent-method"></a>Metodo CBaseFilter.NotifyEvent

Il `NotifyEvent` metodo invia una notifica degli eventi al gestore del grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EventCode* 
</dt> <dd>

Codice di notifica degli eventi.

</dd> <dt>

*EventParam1* 
</dt> <dd>

Primo parametro dell'evento.

</dd> <dt>

*EventParam2* 
</dt> <dd>

Secondo parametro dell'evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili sono quelli riportati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Il gestore del grafico del filtro non accetta notifiche degli eventi.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione completata.<br/>                                                                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Il filtro non ha un puntatore [**all'interfaccia IMediaEventSink.**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)<br/> |



 

## <a name="remarks"></a>Commenti

Per un elenco dei codici di notifica e dei valori dei parametri, vedere [Codici di notifica degli eventi.](event-notification-codes.md)

Nella classe di base, se il codice evento è EC COMPLETE, il metodo imposta il parametro \_ *EventParam2* su un puntatore all'interfaccia [**IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




