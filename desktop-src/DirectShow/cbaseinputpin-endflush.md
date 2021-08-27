---
description: Il metodo EndFlush termina un'operazione di scaricamento. Implementa il metodo IPin::EndFlush.
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Metodo CBaseInputPin.EndFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fba4c82679ebe96827cd45c9045080fb354cdab25eb562523869e97d533c5f2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056351"
---
# <a name="cbaseinputpinendflush-method"></a>Metodo CBaseInputPin.EndFlush

Il `EndFlush` metodo termina un'operazione di scaricamento. Implementa il [**metodo IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo imposta il flag [**\_ BFlushing CBaseInputPin::m**](cbaseinputpin-m-bflushing.md) su **TRUE,** che consente al metodo [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) di accettare gli esempi.

La classe derivata deve eseguire l'override di questo metodo ed eseguire la procedura seguente:

1.  Liberare tutti i dati memorizzati nel buffer e attendere che tutti gli esempi in coda siano eliminati.
2.  Cancellare tutte le notifiche [**EC \_ COMPLETE in**](ec-complete.md) sospeso.
3.  Chiamare il metodo della classe base.
4.  Chiamare [**IPin::EndFlush sui**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) pin di input downstream. Se il pin non ha ancora fornito campioni di supporti a valle, è possibile ignorare questo passaggio. Se i pin di output derivano dalla [**classe CBaseOutputPin,**](cbaseoutputpin.md) è possibile chiamare il metodo [**CBaseOutputPin::D eliverEndFlush.**](cbaseoutputpin-deliverendflush.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




