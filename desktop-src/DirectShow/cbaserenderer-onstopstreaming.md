---
description: Il metodo OnStopStreaming viene chiamato quando il filtro interrompe lo streaming.
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: Metodo CBaseRenderer.OnStopStreaming (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c61490a0719ce45d9776982b9230734d1126cef747330bb595c205500aca331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157664"
---
# <a name="cbaserendereronstopstreaming-method"></a>Metodo CBaseRenderer.OnStopStreaming

Il `OnStopStreaming` metodo viene chiamato quando il filtro arresta lo streaming.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il [**metodo CBaseRenderer::StopStreaming**](cbaserenderer-stopstreaming.md) chiama questo metodo. Non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




