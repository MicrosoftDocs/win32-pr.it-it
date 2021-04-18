---
description: 'Il metodo Notify notifica al pin che è richiesta una modifica di qualità. Questo metodo implementa il metodo IQualityControl:: Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Metodo CTransformOutputPin. Notify (Transfrm. h)
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
ms.openlocfilehash: d6ace7e25f1413f6e17a4d19ef937732ea8c689a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330840"
---
# <a name="ctransformoutputpinnotify-method"></a>Metodo CTransformOutputPin. Notify

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

Puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro che ha recapitato il messaggio di controllo di qualità.

</dd> <dt>

*d* 
</dt> <dd>

Struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo di qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Esito positivo.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ non \_ trovato**</dt> </dl> | Impossibile trovare un oggetto per accettare il messaggio.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) del filtro. Se il filtro non gestisce il messaggio di qualità, questo metodo chiama il metodo [**CBaseInputPin::P assnotify**](cbaseinputpin-passnotify.md) sul pin di input del filtro. Il metodo **PassNotify** passa il messaggio di qualità upstream (o a un gestore di qualità personalizzato, se ne è stato installato uno).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




