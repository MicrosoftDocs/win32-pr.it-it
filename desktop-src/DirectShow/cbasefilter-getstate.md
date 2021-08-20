---
description: Il metodo GetState recupera lo stato dei filtri (in esecuzione, arrestato o sospeso). Questo metodo implementa il metodo IMediaFilter::GetState.
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Metodo CBaseFilter.GetState (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b6ed61b8b1e72652e9590d11827322256d4923bd92405206e5c5419cd5e7ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017169"
---
# <a name="cbasefiltergetstate-method"></a>Metodo CBaseFilter.GetState

Il `GetState` metodo recupera lo stato dei filtri (in esecuzione, arrestato o sospeso). Questo metodo implementa il [**metodo IMediaFilter::GetState.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)

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

Puntatore a una variabile che riceve un membro del tipo enumerato [**FILTER \_ STATE,**](/windows/win32/api/strmif/ne-strmif-filter_state) che indica lo stato del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o \_ PUNTATORE E.

## <a name="remarks"></a>Commenti

Nella classe di base tutte le transizioni di stato sono sincrone e il *parametro dwMilliSecsTimeout* viene ignorato. Se una classe derivata esegue transizioni di stato asincrone, deve eseguire l'override di questo metodo per attendere le transizioni di stato, con un timeout di *dwMilliSecsTimeout* millisecondi.

Se il filtro non recapita i dati mentre è in pausa, eseguire l'override del metodo per restituire il valore VFW S CANT CUE quando il filtro è in pausa `GetState` \_ \_ \_ (vedere [Distribuzione di esempi).](delivering-samples.md) Esempio:


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




