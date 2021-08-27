---
description: Il metodo NotifyFilterState invia una notifica al pin quando cambia lo stato del filtro.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Metodo CBaseStreamControl.NotifyFilterState (Strmctl.h)
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
ms.openlocfilehash: a3433e5c40f86a9e333696774fe671eb7bb90d9803cb9cd6501d7971111e5d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131421"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a>Metodo CBaseStreamControl.NotifyFilterState

Il `NotifyFilterState` metodo invia una notifica al pin quando cambia lo stato del filtro.

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

Specifica il nuovo stato, come membro [**dell'enumerazione FILTER \_ STATE.**](/windows/win32/api/strmif/ne-strmif-filter_state)

</dd> <dt>

*tStart* 
</dt> <dd>

Specifica l'ora di inizio. Se il nuovo stato del filtro è State \_ Running, passare il valore dal [**metodo IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) In caso contrario, usare il valore predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo causa l'interruzione dell'attesa del metodo [**CBaseStreamControl::CheckStreamState.**](cbasestreamcontrol-checkstreamstate.md) Chiamare questo metodo ogni volta che lo stato del filtro proprietario cambia.

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
| Intestazione<br/>  | <dl> <dt>Strmctl.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




