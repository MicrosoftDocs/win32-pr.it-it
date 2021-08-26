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
ms.openlocfilehash: e4bef01168eb7bad9a1ffc8e5e8555ecd5e8804893269723c8dba72a066b3c50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079281"
---
# <a name="ctransinplacefiltergetpin-method"></a>Metodo CTransInPlaceFilter.GetPin

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

Questo metodo esegue l'override [**del metodo CTransformFilter::GetPin.**](ctransformfilter-getpin.md) La prima volta che viene chiamato il metodo , vengono creati entrambi i pin.

Questo metodo non incrementa il conteggio dei riferimenti sul pin restituito, quindi il pin restituito non ha un conteggio dei riferimenti in sospeso. Se il chiamante deve mantenere un riferimento sul pin, deve chiamare il metodo **IUnknown::AddRef** sul pin.

Se il filtro usa i pin [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) predefiniti, probabilmente non è necessario eseguire l'override di questo metodo. Se il filtro usa pin che estendono tali classi, tuttavia, è necessario eseguire l'override di questo metodo per creare pin di quel tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




