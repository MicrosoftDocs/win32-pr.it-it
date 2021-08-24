---
description: Il metodo GetState recupera lo stato dell'oggetto (in esecuzione, arrestato o sospeso). Questo metodo implementa il metodo IMediaFilter::GetState.
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Metodo CBaseMediaFilter.GetState (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a4c70412311be5ea4843a823e961fae34de2974f7365f51286ff6da36e41dcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966701"
---
# <a name="cbasemediafiltergetstate-method"></a>Metodo CBaseMediaFilter.GetState

Il `GetState` metodo recupera lo stato dell'oggetto (in esecuzione, arrestato o sospeso). Questo metodo implementa il [**metodo IMediaFilter::GetState.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwMilliSecsTimeout* 
</dt> <dd>

Intervallo di timeout, in millisecondi.

</dd> <dt>

*State* 
</dt> <dd>

Puntatore a una variabile che riceve un membro del tipo enumerato [**FILTER \_ STATE,**](/windows/win32/api/strmif/ne-strmif-filter_state) che indica lo stato dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o \_ PUNTATORE E.

## <a name="remarks"></a>Commenti

Nella classe di base tutte le transizioni di stato sono sincrone e il *parametro dwMilliSecsTimeout* viene ignorato. Se una classe derivata esegue transizioni di stato asincrone, deve eseguire l'override di questo metodo per attendere le transizioni di stato, con un timeout di *dwMilliSecsTimeout* millisecondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




