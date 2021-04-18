---
description: 'Il metodo Notify notifica al pin che è richiesta una modifica di qualità. Questo metodo implementa il metodo IQualityControl:: Notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Metodo CBaseInputPin. Notify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae7ca47c5adc11c87a739e8736ba327dc0b65f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330939"
---
# <a name="cbaseinputpinnotify-method"></a>Metodo CBaseInputPin. Notify

Il `Notify` metodo notifica al pin che è richiesta una modifica di qualità. Questo metodo implementa il metodo [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSelf* 
</dt> <dd>

Puntatore al filtro che sta inviando il messaggio di controllo di qualità.

</dd> <dt>

*d* 
</dt> <dd>

Struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo della qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

I filtri di solito passano messaggi di controllo della qualità a un pin di output upstream, non a un pin di input. Pertanto, questo metodo restituisce \_ OK senza eseguire alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> <dt>

[Gestione controllo qualità](quality-control-management.md)
</dt> </dl>

 

 




