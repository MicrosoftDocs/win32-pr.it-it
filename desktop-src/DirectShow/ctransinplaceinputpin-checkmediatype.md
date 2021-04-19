---
description: Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Metodo CTransInPlaceInputPin. CheckMediaType (Transip. h)
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
ms.openlocfilehash: 22f271759bc0ade6b820aed2039bbc16a2cf4a31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326203"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a>CTransInPlaceInputPin. CheckMediaType, metodo

Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il tipo di supporto proposto è accettabile. In caso contrario, restituisce \_ false o un codice di errore.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CTransformInputPin:: CheckMediaType**](ctransforminputpin-checkmediatype.md) . Chiama il metodo [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per verificare il tipo di input. Se il pin di output è connesso, questo metodo chiama anche il metodo [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di input downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




