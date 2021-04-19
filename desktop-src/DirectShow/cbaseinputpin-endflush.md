---
description: "Il metodo EndFlush termina un'operazione di svuotamento. Implementa il metodo IPin:: EndFlush."
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Metodo CBaseInputPin. EndFlush (Amfilter. h)
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
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326067"
---
# <a name="cbaseinputpinendflush-method"></a>CBaseInputPin. EndFlush, metodo

Il `EndFlush` metodo termina un'operazione di svuotamento. Implementa il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo imposta il flag [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) su **true**, che consente al metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) di accettare esempi.

La classe derivata deve eseguire l'override di questo metodo ed eseguire i passaggi seguenti:

1.  Liberare i dati memorizzati nel buffer e attendere che tutti gli esempi in coda vengano eliminati.
2.  Cancellare le notifiche [**\_ complete di EC**](ec-complete.md) in sospeso.
3.  Chiamare il metodo della classe base.
4.  Chiamare [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) nei pin di input downstream. Se il PIN non ha ancora recapitato alcun campione multimediale a valle, è possibile ignorare questo passaggio. Se i pin di output derivano dalla classe [**CBaseOutputPin**](cbaseoutputpin.md) , è possibile chiamare il metodo [**CBaseOutputPin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




