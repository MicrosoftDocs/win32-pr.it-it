---
description: Il metodo IsEndOfStreamDelivered esegue una query per determinare se l' \_ evento EC complete è stato recapitato al gestore del grafico dei filtri.
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: Metodo CBaseRenderer. IsEndOfStreamDelivered (Renbase. h)
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
ms.openlocfilehash: f60216afc6481411010fb2f2b0618c36a7d7acf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330053"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a>CBaseRenderer. IsEndOfStreamDelivered, metodo

Il `IsEndOfStreamDelivered` metodo esegue una query che indica se l' \_ evento di completamento EC è stato recapitato al gestore del grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il flag [**CBaseRenderer:: m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




