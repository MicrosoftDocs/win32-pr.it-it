---
description: "Metodo CDynamicOutputPin.DeliverBeginFlush: il metodo DeliverBeginFlush richiede al pin di input connesso di iniziare un'operazione di scaricamento."
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Metodo CDynamicOutputPin.DeliverBeginFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4158a3d6191325e8b647e4551133952d623f795
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099319"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a>Metodo CDynamicOutputPin.DeliverBeginFlush

Il `DeliverBeginFlush` metodo richiede al pin di input connesso di iniziare un'operazione di scaricamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseOutputPin::D eliverBeginFlush.**](cbaseoutputpin-deliverbeginflush.md) Imposta [**l'evento \_ HStopEvent CDynamicOutputPin::m.**](cdynamicoutputpin-m-hstopevent.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




