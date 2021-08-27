---
description: Il metodo Next recupera un numero specificato di tipi di supporti. Questo metodo implementa il metodo IEnumMediaTypes::Next.
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Metodo CEnumMediaTypes.Next (Amfilter.h)
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
ms.openlocfilehash: f8dd593fe6ca550c55ffc1f769a303dd2d5cbf7a8d8c986be8a39278d7f334ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131291"
---
# <a name="cenummediatypesnext-method"></a>Metodo CEnumMediaTypes.Next

Il `Next` metodo recupera un numero specificato di tipi di supporti. Questo metodo implementa il [**metodo IEnumMediaTypes::Next.**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next)

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

Numero di tipi di supporti da recuperare.

</dd> <dt>

*ppMediaTypes* 
</dt> <dd>

Matrice di puntatori a [**strutture AM \_ MEDIA \_ TYPE,**](/windows/win32/api/strmif/ns-strmif-am_media_type) di dimensioni *cPins*.

</dd> <dt>

*pcFetched* 
</dt> <dd>

Puntatore a una variabile che riceve il numero di tipi di supporti restituiti dal metodo. Può essere **NULL** se *cMediaTypes* è 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Non è stato recuperato il numero di tipi di supporti richiesto.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Operazione completata.<br/>                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argomento non valido.<br/>                                                        |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>                  | Argomento del puntatore **NULL.**<br/>                                               |
| <dl> <dt>**ENUMERAZIONE VFW \_ \_ NON \_ \_ \_ SINCRONIZZATA**</dt> </dl> | Lo stato del pin è stato modificato ed è ora incoerente con l'enumeratore.<br/> |



 

## <a name="remarks"></a>Commenti

Se il metodo ha esito positivo, la matrice specificata da *ppMediaTypes* contiene puntatori alle strutture AM \_ MEDIA \_ TYPE. Il numero di strutture è uguale a *\* pcFetched*. Liberare ogni tipo di supporto chiamando la [**funzione DeleteMediaType.**](deletemediatype.md)

Questo metodo chiama il metodo [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) del pin per recuperare i tipi di supporti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




