---
description: 'Il metodo EnumMediaTypes enumera i tipi di supporto preferiti del PIN. Questo metodo implementa il metodo IPin:: EnumMediaTypes.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Metodo CBasePin. EnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54aaddbbcde26791b6c55665bfbbb7ff62048238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328848"
---
# <a name="cbasepinenummediatypes-method"></a>CBasePin. EnumMediaTypes, metodo

Il `EnumMediaTypes` metodo enumera i tipi di supporto preferiti del PIN. Questo metodo implementa il metodo [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>       |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null** .<br/> |



 

## <a name="remarks"></a>Commenti

I pin di input non sono necessari per enumerare i tipi preferiti. I pin di output devono enumerare almeno un tipo preferito. In caso contrario, entrambi i pin potrebbero non avere un tipo preferito, rendendo impossibile la connessione.

L'interfaccia **IEnumMediaTypes** funziona come un enumeratore COM standard. Per altre informazioni, vedere [enumerazione di oggetti in un grafico a filtro](enumerating-objects-in-a-filter-graph.md). Se il metodo ha esito positivo, l'interfaccia **IEnumMediaTypes** ha un conteggio dei riferimenti in attesa. Assicurarsi di rilasciarlo al termine dell'operazione.

La classe base [**CEnumMediaTypes**](cenummediatypes.md) implementa **IEnumMediaTypes**. Chiama il metodo [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) del PIN per enumerare i tipi di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




