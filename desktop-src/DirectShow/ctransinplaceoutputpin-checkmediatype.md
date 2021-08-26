---
description: 'Metodo CTransInPlaceOutputPin.CheckMediaType: il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.'
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Metodo CTransInPlaceOutputPin.CheckMediaType (Transip.h)
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
ms.openlocfilehash: 2816d148af2a7514dc28a71036402f3781e47a0144848a2ea81bbb94d339f961
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999031"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a>Metodo CTransInPlaceOutputPin.CheckMediaType

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Operazione completata.<br/>                 |
| <dl> <dt>**TIPO E VFW \_ \_ NON \_ \_ ACCETTATO**</dt> </dl> | Tipo di supporto non accettato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CTransformOutputPin::CheckMediaType.**](ctransformoutputpin-checkmediatype.md)

Se il filtro è già in streaming e usa due allocatori, questo metodo rifiuta qualsiasi modifica di formato. In caso contrario, questo metodo chiama il metodo [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per controllare il tipo di supporto. Se il pin di input è connesso, chiama anche il metodo [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di output upstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




