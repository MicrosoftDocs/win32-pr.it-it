---
description: Il metodo Notify riceve una notifica di richiesta di modifica della qualità.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Metodo CBaseVideoRenderer. Notify (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326564"
---
# <a name="cbasevideorenderernotify-method"></a>Metodo CBaseVideoRenderer. Notify

Il `Notify` metodo riceve una notifica che viene richiesta una modifica di qualità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSelf* \[ in\]
</dt> <dd>

Puntatore al filtro che invia la notifica di qualità.

</dd> <dt>

*domande* e risposte \[\]
</dt> <dd>

Struttura delle notifiche di qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) nel renderer video. Questo metodo viene chiamato, in genere da Filter Graph Manager, quando è necessario tagliare la qualità. Questo problema può verificarsi quando la qualità della riproduzione audio è stata aumentata fino a quando la qualità della riproduzione video deve essere ridotta.

`Notify` imposta il membro dati **\_ trThrottle m** su un valore delay da inserire tra i frame da [**ThrottleWait**](cbasevideorenderer-throttlewait.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




