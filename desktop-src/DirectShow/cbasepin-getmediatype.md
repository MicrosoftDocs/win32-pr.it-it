---
description: 'Metodo CBasePin.GetMediaType: il metodo GetMediaType recupera un tipo di supporto preferito, in base al valore di indice.'
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Metodo CBasePin.GetMediaType (Amfilter.h)
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
ms.openlocfilehash: 186f2eddbedf4eb0565a4ca66ff4ed7e5b080090
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099369"
---
# <a name="cbasepingetmediatype-method"></a>Metodo CBasePin.GetMediaType

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

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione completata.<br/>              |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Indice non compreso nell'intervallo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Indice minore di zero.<br/> |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl>           | Errore imprevisto.<br/>     |



 

## <a name="remarks"></a>Commenti

Dall'elenco dei tipi di supporti preferiti, questo metodo restituisce il tipo con un valore di indice *iPosition*. La [**classe CEnumMediaTypes**](cenummediatypes.md) chiama questo metodo per enumerare i tipi di supporti preferiti.

La classe base restituisce E \_ UNEXPECTED. Eseguire l'override di questo metodo nella classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




