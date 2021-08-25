---
description: 'Metodo CBasePin.Notify: il metodo Notify notifica al pin che è richiesta una modifica della qualità. Questo metodo implementa il metodo IQualityControl::Notify.'
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
ms.openlocfilehash: 0e74a8880e446300ca142bfcf28633d267d184178a0c3572c3a8049667536978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910441"
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

Specifica una [**struttura Quality**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La classe base restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

I pin di output devono eseguire l'override di questo metodo per accettare messaggi di controllo qualità.

Se è stato installato un quality manager esterno (vedere [**CBasePin::SetSink),**](cbasepin-setsink.md)passare il messaggio a tale responsabile qualità. In caso contrario, il filtro deve gestire il messaggio stesso o passare il messaggio a monte. Per altre informazioni, vedere [Quality-Control Management](quality-control-management.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




