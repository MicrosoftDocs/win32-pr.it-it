---
description: Il metodo GetMediaType recupera un tipo di supporto preferito per il pin di output.
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Metodo CTransformFilter. GetMediaType (Transfrm. h)
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
ms.openlocfilehash: ba751e291a1ffa8e030be7e77cfd456956718baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331312"
---
# <a name="ctransformfiltergetmediatype-method"></a>CTransformFilter. GetMediaType, metodo

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

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Esito positivo.<br/>              |
| <dl> <dt>**\_non ci \_ sono \_ altri \_ elementi di VFW**</dt> </dl> | Indice non compreso nell'intervallo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Indice minore di zero.<br/> |



 

## <a name="remarks"></a>Commenti

Il metodo [**CTransformOutputPin:: GetMediaType**](ctransformoutputpin-getmediatype.md) del PIN di output chiama questo metodo. La classe derivata deve implementare questo metodo. Per ulteriori informazioni, vedere [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




