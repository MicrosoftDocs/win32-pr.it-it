---
description: "Il metodo GetState recupera lo stato dell'oggetto (in esecuzione, arrestato o sospeso). Questo metodo implementa il metodo IMediaFilter:: GetState."
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Metodo CBaseMediaFilter. GetState (Amfilter. h)
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
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325382"
---
# <a name="cbasemediafiltergetstate-method"></a>Metodo CBaseMediaFilter. GetState

Il `GetState` metodo recupera lo stato dell'oggetto (in esecuzione, arrestato o sospeso). Questo metodo implementa il metodo [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .

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

Puntatore a una variabile che riceve un membro del tipo enumerato [**\_ dello stato del filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , che indica lo stato dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un \_ puntatore S OK o e \_ .

## <a name="remarks"></a>Commenti

Nella classe di base tutte le transizioni di stato sono sincrone e il parametro *dwMilliSecsTimeout* viene ignorato. Se una classe derivata esegue transizioni di stato asincrone, deve eseguire l'override di questo metodo per attendere durante le transizioni di stato, con un timeout di *dwMilliSecsTimeout* millisecondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




