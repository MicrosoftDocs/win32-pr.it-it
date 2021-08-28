---
description: Il metodo SetFilterGraph specifica il sink di evento per gli eventi di controllo del flusso.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Metodo CBaseStreamControl.SetFilterGraph (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 304ec081ce7087d822ce3382bf4784c05cbc8782fadb3cdfee887f6bd8f0acfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502641"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a>Metodo CBaseStreamControl.SetFilterGraph

Il `SetFilterGraph` metodo specifica il sink di evento per gli eventi di controllo del flusso.

## <a name="syntax"></a>Sintassi


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSink* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) di Filter Graph Manager o **NULL** quando il filtro esce dal grafico dei filtri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Chiamare questo metodo dall'interno del metodo [**IBaseFilter::JoinFilterGraph del**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) filtro. La **classe CBaseStreamControl** usa **l'interfaccia IMediaEventSink** per inviare eventi [**EC STREAM CONTROL \_ \_ \_ STARTED**](ec-stream-control-started.md) ed [**EC STREAM CONTROL \_ \_ \_ STOPPED.**](ec-stream-control-stopped.md)

Se il filtro deriva da **CBaseFilter,** chiamare prima il metodo [**CBaseFilter::JoinFilterGraph,**](cbasefilter-joinfiltergraph.md) che imposta la variabile membro [**CBaseFilter::m \_ pSink.**](cbasefilter-m-psink.md) Passare quindi **m \_ pSink** al `SetFilterGraph` metodo . Si noti **che m \_ pSink** è **NULL** quando il filtro esce dal grafico, che è corretto.

## <a name="examples"></a>Esempio


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
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

 

 




