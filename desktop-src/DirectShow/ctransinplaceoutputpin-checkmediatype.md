---
description: Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Metodo CTransInPlaceOutputPin. CheckMediaType (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0a422851bc7e09075076decc39d57b85d1052ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326184"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a>CTransInPlaceOutputPin. CheckMediaType, metodo

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

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                 |
| <dl> <dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt> </dl> | Tipo di supporto non accettato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CTransformOutputPin:: CheckMediaType**](ctransformoutputpin-checkmediatype.md) .

Se il filtro è già in streaming e usa due allocatori, questo metodo rifiuterà eventuali modifiche al formato. In caso contrario, questo metodo chiama il metodo [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per verificare il tipo di supporto. Se il pin di input è connesso, viene chiamato anche il metodo [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di output upstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




