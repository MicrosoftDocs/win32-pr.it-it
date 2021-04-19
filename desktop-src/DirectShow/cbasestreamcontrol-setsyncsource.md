---
description: Il metodo SetSyncSource notifica alla classe di base il clock di riferimento corrente.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Metodo CBaseStreamControl. SetSyncSource (Strmctl. h)
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
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324030"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a>CBaseStreamControl. SetSyncSource, metodo

Il `SetSyncSource` metodo notifica alla classe di base l'orologio di riferimento corrente.

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

Puntatore all'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) dell'orologio di riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Chiamare questo metodo dall'interno del metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) del filtro. La classe **CBaseStreamControl** usa l'interfaccia **IReferenceClock** per assicurarsi che non elimini troppo rapidamente i campioni.

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
| Intestazione<br/>  | <dl> <dt>Strmctl. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




