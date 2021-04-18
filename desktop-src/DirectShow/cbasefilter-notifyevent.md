---
description: Il metodo NotifyEvent invia una notifica degli eventi al gestore del grafico dei filtri.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Metodo CBaseFilter. NotifyEvent (Amfilter. h)
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
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332079"
---
# <a name="cbasefilternotifyevent-method"></a>CBaseFilter. NotifyEvent, metodo

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

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Il gestore del grafico del filtro non accetta le notifiche degli eventi.<br/>                              |
| <dl> <dt>**\_OK**</dt> </dl>      | Esito positivo.<br/>                                                                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Il filtro non dispone di un puntatore all'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .<br/> |



 

## <a name="remarks"></a>Commenti

Per un elenco di codici di notifica e valori di parametri, vedere [codici di notifica degli eventi](event-notification-codes.md).

Nella classe di base, se il codice dell'evento è EC \_ completo, il metodo imposta il parametro *EventParam2* su un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




