---
description: 'Metodo CTransInPlaceInputPin.CheckMediaType: il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.'
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Metodo CTransInPlaceInputPin.CheckMediaType (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91a1889e9c8a4060b734449df9f73474c16d1aec09d6534de048359ced156958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654844"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a>Metodo CTransInPlaceInputPin.CheckMediaType

Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il tipo di supporto proposto è accettabile. In caso contrario, restituisce S \_ FALSE o un codice di errore.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CTransformInputPin::CheckMediaType.**](ctransforminputpin-checkmediatype.md) Chiama il metodo [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per controllare il tipo di input. Se il pin di output è connesso, questo metodo chiama anche il metodo [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di input downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




