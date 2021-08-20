---
description: Il metodo SetSyncSource notifica la classe di base dell'orologio di riferimento corrente.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Metodo CBaseStreamControl.SetSyncSource (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2b7fa5a4f627b33bbca1665e3d1ff2c5bc347cfa0e35adec37e0afffa81f198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954780"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a>Metodo CBaseStreamControl.SetSyncSource

Il `SetSyncSource` metodo notifica la classe di base dell'orologio di riferimento corrente.

## <a name="syntax"></a>Sintassi


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRefClock* 
</dt> <dd>

Puntatore [**all'interfaccia IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del clock di riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Chiamare questo metodo dall'interno del metodo [**IMediaFilter::SetSyncSource del**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) filtro. La **classe CBaseStreamControl** usa **l'interfaccia IReferenceClock** per assicurarsi che non scarti gli esempi troppo rapidamente.

## <a name="examples"></a>Esempio


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




