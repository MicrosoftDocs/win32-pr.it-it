---
description: "Metodo CDynamicOutputPin.DeliverEndFlush: il metodo DeliverEndFlush richiede al pin di input connesso di terminare un'operazione di scaricamento."
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Metodo CDynamicOutputPin.DeliverEndFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cdd7e26b0c08b154c6cffd08066e8ae841a6aa849db4751ffa0cdf252848719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055951"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>Metodo CDynamicOutputPin.DeliverEndFlush

Il `DeliverEndFlush` metodo richiede al pin di input connesso di terminare un'operazione di scaricamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseOutputPin::D eliverEndFlush.**](cbaseoutputpin-deliverendflush.md) Reimposta [**l'evento CDynamicOutputPin::m \_ hStopEvent.**](cdynamicoutputpin-m-hstopevent.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




