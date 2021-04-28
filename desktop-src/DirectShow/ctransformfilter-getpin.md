---
description: 'Metodo CTransformFilter.GetPin: il metodo GetPin recupera un pin.'
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: Metodo CTransformFilter.GetPin (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e76cafce2ca5a9881b87d9248c144dc584971c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085079"
---
# <a name="ctransformfiltergetpin-method"></a>Metodo CTransformFilter.GetPin

Il `GetPin` metodo recupera un pin.

## <a name="syntax"></a>Sintassi


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*n* 
</dt> <dd>

Numero del pin specificato, indicizzato da zero. In questo filtro, pin 0 è il pin di input e pin 1 è il pin di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore [**all'oggetto CBasePin**](cbasepin.md) che implementa il pin oppure **NULL** se il metodo ha esito negativo.

## <a name="remarks"></a>Commenti

Questo metodo implementa il metodo [**CBaseFilter::GetPin**](cbasefilter-getpin.md) virtuale puro. La prima volta che viene chiamato il metodo , vengono creati entrambi i pin.

Questo metodo non incrementa il conteggio dei riferimenti sul pin restituito, quindi il pin restituito non ha un conteggio dei riferimenti in sospeso. Se il chiamante deve mantenere un riferimento sul pin, deve chiamare il metodo **IUnknown::AddRef** sul pin.

Se il filtro usa i pin [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin**](ctransformoutputpin.md) predefiniti, probabilmente non è necessario eseguire l'override di questo metodo. Se il filtro usa pin che estendono tali classi, tuttavia, è necessario eseguire l'override di questo metodo per creare pin di quel tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




