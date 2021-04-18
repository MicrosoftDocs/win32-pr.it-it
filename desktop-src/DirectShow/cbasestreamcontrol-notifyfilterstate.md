---
description: Il metodo NotifyFilterState invia una notifica al pin quando lo stato del filtro viene modificato.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Metodo CBaseStreamControl. NotifyFilterState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ccb96361c8f4938bd95ffdc29229a035a239cc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331648"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a>CBaseStreamControl. NotifyFilterState, metodo

Il `NotifyFilterState` metodo invia una notifica al pin quando lo stato del filtro viene modificato.

## <a name="syntax"></a>Sintassi


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nuovo \_ stato* 
</dt> <dd>

Specifica il nuovo stato, come membro dell'enumerazione [**\_ dello stato del filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) .

</dd> <dt>

*tStart* 
</dt> <dd>

Specifica l'ora di inizio. Se lo stato del nuovo filtro è \_ Running, passare il valore dal metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) . In caso contrario, usare il valore predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo fa in modo che il metodo [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) interrompa l'attesa. Chiamare questo metodo ogni volta che il filtro proprietario modifica lo stato.

## <a name="examples"></a>Esempio


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




