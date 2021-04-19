---
description: 'Il metodo successivo recupera un numero specificato di tipi di supporti. Questo metodo implementa il metodo IEnumMediaTypes:: Next.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Metodo CEnumMediaTypes. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329852"
---
# <a name="cenummediatypesnext-method"></a>Metodo CEnumMediaTypes. Next

Il `Next` metodo recupera un numero specificato di tipi di supporti. Questo metodo implementa il metodo [**IEnumMediaTypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Numero di tipi di supporto da recuperare.

</dd> <dt>

*ppMediaTypes* 
</dt> <dd>

Matrice di puntatori alle strutture di [**\_ \_ tipo multimediale am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , di dimensioni *cPins*.

</dd> <dt>

*pcFetched* 
</dt> <dd>

Puntatore a una variabile che riceve il numero di tipi di supporti restituiti dal metodo. Può essere **null** se *cMediaTypes* è 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Non è stato possibile recuperare tutti i tipi di supporto richiesti.<br/>                       |
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argomento non valido.<br/>                                                        |
| <dl> <dt>**\_puntatore E**</dt> </dl>                  | Argomento puntatore **null** .<br/>                                               |
| <dl> <dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt> </dl> | Lo stato del PIN è stato modificato ed è ora incoerente con l'enumeratore.<br/> |



 

## <a name="remarks"></a>Commenti

Se il metodo ha esito positivo, la matrice specificata da *ppMediaTypes* contiene i puntatori alle \_ strutture del tipo di supporto am \_ . Il numero di strutture è uguale a *\* pcFetched*. Liberare ogni tipo di supporto chiamando la funzione [**DeleteMediaType**](deletemediatype.md) .

Questo metodo chiama il metodo [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) del PIN per recuperare i tipi di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




