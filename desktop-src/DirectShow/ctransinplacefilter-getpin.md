---
description: Il metodo GetPin recupera un PIN.
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Metodo CTransInPlaceFilter. GetPin (Transip. h)
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
ms.openlocfilehash: ae93b663af5427bc61367ae03a3abd6790b8634a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331121"
---
# <a name="ctransinplacefiltergetpin-method"></a>CTransInPlaceFilter. GetPin, metodo

Il `GetPin` metodo recupera un PIN.

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

Numero del PIN specificato, indicizzato da zero. In questo filtro, pin 0 è il pin di input e pin 1 è il pin di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'oggetto [**CBasePin**](cbasepin.md) che implementa il PIN oppure **null** se il metodo ha esito negativo.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) . La prima volta che viene chiamato il metodo, vengono creati entrambi i pin.

Questo metodo non incrementa il conteggio dei riferimenti sul pin restituito, quindi il pin restituito non dispone di un conteggio dei riferimenti in attesa. Se il chiamante deve mantenere un riferimento al pin, deve chiamare il metodo **IUnknown:: AddRef** sul pin.

Se il filtro usa i pin predefiniti [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) , probabilmente non è necessario eseguire l'override di questo metodo. Se il filtro usa pin che estendono tali classi, tuttavia, è necessario eseguire l'override di questo metodo per creare pin di quel tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




