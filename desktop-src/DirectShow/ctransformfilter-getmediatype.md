---
description: 'Metodo CTransformFilter.GetMediaType: il metodo GetMediaType recupera un tipo di supporto preferito per il pin di output.'
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Metodo CTransformFilter.GetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b471ac42ceb44f5e65a2ac08365bf97ab0e3157816b772b331cde0fa0b13bde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907531"
---
# <a name="ctransformfiltergetmediatype-method"></a>Metodo CTransformFilter.GetMediaType

Il `GetMediaType` metodo recupera un tipo di supporto preferito per il pin di output.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iPosition* 
</dt> <dd>

Valore di indice in base zero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Puntatore a [**un oggetto CMediaType**](cmediatype.md) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione completata.<br/>              |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Indice non compreso nell'intervallo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Indice minore di zero.<br/> |



 

## <a name="remarks"></a>Commenti

Il metodo [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) del pin di output chiama questo metodo. La classe derivata deve implementare questo metodo. Per altre informazioni, vedere [**CBasePin::GetMediaType.**](cbasepin-getmediatype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




