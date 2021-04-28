---
description: 'Metodo CBasePin.EnumMediaTypes: il metodo EnumMediaTypes enumera i tipi di supporti preferiti del pin. Questo metodo implementa il metodo IPin::EnumMediaTypes.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Metodo CBasePin.EnumMediaTypes (Amfilter.h)
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
ms.openlocfilehash: c68fe1ab83724149dcd2fb58a60e9c6950d887ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099389"
---
# <a name="cbasepinenummediatypes-method"></a>Metodo CBasePin.EnumMediaTypes

Il `EnumMediaTypes` metodo enumera i tipi di supporti preferiti del pin. Questo metodo implementa il [**metodo IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)

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

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili sono quelli riportati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>       |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Argomento del puntatore **NULL.**<br/> |



 

## <a name="remarks"></a>Commenti

I pin di input non sono necessari per enumerare i tipi preferiti. I pin di output devono enumerare almeno un tipo preferito. In caso contrario, entrambi i pin potrebbero non avere un tipo preferito, rendendo impossibile una connessione.

**L'interfaccia IEnumMediaTypes** funziona come un enumeratore COM standard. Per altre informazioni, vedere [Enumerazione di oggetti in un grafo di filtro.](enumerating-objects-in-a-filter-graph.md) Se il metodo ha esito positivo, **l'interfaccia IEnumMediaTypes** ha un conteggio dei riferimenti in sospeso. Al termine, assicurarsi di rilasciarlo.

La classe di base [**CEnumMediaTypes**](cenummediatypes.md) implementa **IEnumMediaTypes**. Chiama il metodo [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) del pin per enumerare i tipi di supporti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




