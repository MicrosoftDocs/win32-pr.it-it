---
description: Il metodo IsEndOfStreamDelivered esegue una query per determinare se l'evento EC COMPLETE è stato \_ recapitato al gestore del grafico filtri.
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: Metodo CBaseRenderer.IsEndOfStreamDelivered (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStreamDelivered
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f15c2bca14e6c0f55f46441bbb4de362e6375d0b67f3012a4ad234a9366b188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954880"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a>Metodo CBaseRenderer.IsEndOfStreamDelivered

Il `IsEndOfStreamDelivered` metodo esegue una query per determinare se l'evento EC COMPLETE è stato \_ recapitato al gestore del grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il flag [**CBaseRenderer::m \_ bEOSDelivered.**](cbaserenderer-m-beosdelivered.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




