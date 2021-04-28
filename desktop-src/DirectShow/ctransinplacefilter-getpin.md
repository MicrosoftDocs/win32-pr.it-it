---
description: 'Metodo CTransInPlaceFilter.GetPin: il metodo GetPin recupera un pin.'
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Metodo CTransInPlaceFilter.GetPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084769"
---
# <a name="ctransinplacefiltergetpin-method"></a>Metodo CTransInPlaceFilter.GetPin

Il `GetPin` metodo recupera un segnaposto.

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

Restituisce un puntatore [**all'oggetto CBasePin**](cbasepin.md) che implementa il pin oppure **NULL se** il metodo ha esito negativo.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CTransformFilter::GetPin.**](ctransformfilter-getpin.md) La prima volta che viene chiamato il metodo , vengono creati entrambi i segnaposto.

Questo metodo non incrementa il conteggio dei riferimenti sul segnaposto restituito, quindi il pin restituito non ha un conteggio dei riferimenti in sospeso. Se il chiamante deve mantenere un riferimento sul pin, deve chiamare il metodo **IUnknown::AddRef** sul pin.

Se il filtro usa i pin [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) predefiniti, probabilmente non è necessario eseguire l'override di questo metodo. Se il filtro usa segnaposto che estendono tali classi, tuttavia, è necessario eseguire l'override di questo metodo per creare segnaposti di quel tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




