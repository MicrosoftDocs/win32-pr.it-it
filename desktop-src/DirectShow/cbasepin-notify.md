---
description: 'Metodo CBasePin.Notify: il metodo Notify notifica al pin che è richiesta una modifica di qualità. Questo metodo implementa il metodo IQualityControl::Notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Metodo CBasePin.Notify (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35e751fb583010402df53e1a85eca11f751eda24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096019"
---
# <a name="cbasepinnotify-method"></a>Metodo CBasePin.Notify

Il `Notify` metodo notifica al pin che è richiesta una modifica di qualità. Questo metodo implementa il [**metodo IQualityControl::Notify.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)

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

Puntatore [**all'interfaccia IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro che ha recapitato il messaggio di controllo qualità.

</dd> <dt>

*D* 
</dt> <dd>

Specifica una struttura [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La classe di base restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

I pin di output devono eseguire l'override di questo metodo per accettare messaggi di controllo di qualità.

Se è stato installato un gestore qualità esterno (vedere [**CBasePin::SetSink),**](cbasepin-setsink.md)passare il messaggio a tale responsabile qualità. In caso contrario, il filtro deve gestire il messaggio stesso o passare il messaggio a monte. Per altre informazioni, vedere [Quality-Control Management.](quality-control-management.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




