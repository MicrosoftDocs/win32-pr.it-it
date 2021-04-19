---
description: Il metodo SetFilterGraph specifica il sink di evento per gli eventi di controllo del flusso.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Metodo CBaseStreamControl. SetFilterGraph (Strmctl. h)
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
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324038"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a>CBaseStreamControl. SetFilterGraph, metodo

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

Puntatore all'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) dell'oggetto Filter Graph Manager oppure **null** quando il filtro lascia il grafico del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Chiamare questo metodo dall'interno del metodo [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del filtro. La classe **CBaseStreamControl** usa l'interfaccia **IMediaEventSink** per inviare il controllo del [**flusso EC \_ \_ \_ avviato**](ec-stream-control-started.md) e gli eventi di [**controllo del flusso EC \_ \_ \_ interrotti**](ec-stream-control-stopped.md) .

Se il filtro deriva da **CBaseFilter**, chiamare prima il metodo [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) , che imposta la variabile membro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) . Passare quindi **m \_ pSink** al `SetFilterGraph` metodo. Si noti che **m \_ PSink** è **null** quando il filtro esce dal grafico, che è corretto.

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
| Intestazione<br/>  | <dl> <dt>Strmctl. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




