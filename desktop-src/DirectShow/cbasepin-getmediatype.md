---
description: Il metodo GetMediaType recupera un tipo di supporto preferito, in base al valore di indice.
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Metodo CBasePin. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c54c5cd769a8efa0c720c7050cca45b00b8209e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333605"
---
# <a name="cbasepingetmediatype-method"></a>CBasePin. GetMediaType, metodo

Il `GetMediaType` metodo recupera un tipo di supporto preferito, in base al valore di indice.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
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

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Esito positivo.<br/>              |
| <dl> <dt>**\_non ci \_ sono \_ altri \_ elementi di VFW**</dt> </dl> | Indice non compreso nell'intervallo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Indice minore di zero.<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>           | Errore imprevisto.<br/>     |



 

## <a name="remarks"></a>Commenti

Dall'elenco dei tipi di supporto preferiti del PIN, questo metodo restituisce il tipo con un valore di indice *iPosition*. La classe [**CEnumMediaTypes**](cenummediatypes.md) chiama questo metodo per enumerare i tipi di supporto preferiti.

La classe base restituisce E \_ imprevisto. Eseguire l'override di questo metodo nella classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




