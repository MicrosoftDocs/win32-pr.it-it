---
description: 'Metodo CTransformOutputPin.Notify: il metodo Notify notifica al pin che è richiesta una modifica di qualità. Questo metodo implementa il metodo IQualityControl::Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Metodo CTransformOutputPin.Notify (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69cff051ecab1a93d9fdceac20143bef7d1959ff523aa5893e5ae9c633aa80f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538141"
---
# <a name="ctransformoutputpinnotify-method"></a>Metodo CTransformOutputPin.Notify

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

[**Struttura di**](/windows/win32/api/strmif/ns-strmif-quality) qualità che contiene il messaggio di controllo qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Operazione completata.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ NON \_ TROVATO**</dt> </dl> | Impossibile trovare un oggetto per accettare il messaggio.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CTransformFilter::AlterQuality del**](ctransformfilter-alterquality.md) filtro. Se il filtro non gestisce il messaggio di qualità, questo metodo chiama il metodo [**CBaseInputPin::P assNotify**](cbaseinputpin-passnotify.md) sul pin di input del filtro. Il **metodo PassNotify** passa il messaggio di qualità a monte (o a un responsabile qualità personalizzato, se ne è stato installato uno).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




